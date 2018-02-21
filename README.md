# Setup

1: Assign a container to host the chat widget:
```html
 <div id="root">
      <div id="chat-container">
      </div>
    </div>
```

2: Create the chat widget
```javascript
 <script type="text/javascript">
        var chatWidget = BluBot.widget.new({userId: "test_user",userName:"question_asker"},"chat-container"); //root is the container id where the widget should be placed
        //starts the widget
        chatWidget.start();
        chatWidget.onMessageReceived((activity) => {
           console.log(activity);
        });
     
    </script>
```

3: Start the conversation
To start the conversation you need to run the start command on the widget
```javascript
chatWidget.onMessageReceived((activity) => {
           console.log(activity);
        });
```

4: Listen to messages
Each message that is send by the bot to the user can be monitored using:
```javascript
chatWidget.onMessageReceived((activity) => {
           console.log(activity);
        });
```

# Styles
