README

1. Set up a thing.

1. Edit `mqtt.host` in `mqtt-ws.conf` to refer the endpoint of the thing.
```
{
    "mqtt": {
        "host": "<your-endpoint>",
        "port": 1883
    },
    "websocket": {
        "port": 8080
    }
}
```

1. Edit `thing.js`. Fill `mqttTopic`, `username` and `password`.
```
var thing = {
  mqttTopic: "<your-topic>",
  username: "<your-username>",
  password: "<your-password>",
}
```

1. Install modules
```
$ npm install
```

1. Run the bridge.
```
$ ./node_modules/.bin/mqttwsBridge -c mqtt-ws.conf
```

1. Open `index.html` with your browser
```
$ open index.html    # if MacOSX
```

1. Publish a message to the topic
