# pushbots-nodejs

### Installation
```bash
npm install pushbots
```

### Usage

```javascript

var pushbots = require('pushbots');

var options = {
id:'548ef5901d0ab1f3228b456a',
secret:'646f1ac2fd86ea14ae5a95db7fef724c'
};

var Pushbots = new pushbots.api(options);

Pushbots.setMessage("Hi from new nodeJS API!" ,1);
Pushbots.customFields({"article_id":1234});
Pushbots.customNotificationTitle("CUSTOM TITLE");

Pushbots.push(function(response){
console.log(response);
});
