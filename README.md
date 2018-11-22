dark-slack theme for those that work on the Graveyard shift of just wants a dark theme. 

You will need to place this into the ssb-interop.js file and restart Slack for it to set. Please keep in mind though that updates will overwrite the file so you have to add it to the bottom again. 

```
 document.addEventListener('DOMContentLoaded', function() {
 $.ajax({
   url: 'https://raw.githubusercontent.com/suedeyoung/dark-slack/master/dark.css',
   success: function(css) {
     let overrides = `
     code { background-color: #282A36; color: #85c5ff; } /* Change color: to whatever font color you want */
     .c-mrkdwn__pre, .c-mrkdwn__quote { background: #535353 !important; background-color: #535353 !important; }
     `
     $("<style></style>").appendTo('head').html(css + overrides);
   }
 });
}); 
```
