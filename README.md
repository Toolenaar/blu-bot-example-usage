# Setup

See index.html for all code

## 1: Import the library & fonts:
To use the correct fonts be sure to import the Lato font from google fonts.
```html
<link href="https://fonts.googleapis.com/css?family=Lato:300,400,700" rel="stylesheet">
<script type="text/javascript" src="https://blubot.blob.core.windows.net/jsc/blu-onboarding-bundle.js"></script></head>
```
## 2: Assign a container & position it using css:
Assign a container in which the chat window will be hosted, and position it using css. Remember the id for the next step.
```html
<div id="root">
  <div id="chat-container">
  </div>
</div>
```

## 3: Create the chat widget:
You can specify the userName and userId. For analytic pruposes the userId needs to be unique. If logging in with an anonymous user, a GUID will suffice.
Be sure to provide the right id for the container in which the chat window will be placed.
```javascript
<script type="text/javascript">
    var chatWidget = BluBot.widget.new({userId: "UNIQUE_ID_HERE",userName:"question_asker"},"chat-container");
    //starts the widget
    chatWidget.start();
    chatWidget.onMessageReceived((activity) => {
       console.log(activity);
    });
</script>
```

## 4: Start the conversation:
To start the conversation you need to run the start command on the widget
```javascript
chatWidget.start();
```

## 5: Listen to messages:
Each message that is send by the bot to the user can be monitored using:
```javascript
chatWidget.onMessageReceived((activity) => {
    console.log(activity);
});
```

