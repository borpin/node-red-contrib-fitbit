Makes GET request to the https://dev.fitbit.com/build/reference/web-api/ Fitbit API

Please refer to the API documentation for specific input details, dates should be convertable by https://momentjs.com/docs/ MomentJS.
Some parameters, such as Period, have a limited set of inputs that vary between endpoints

modified to make all the Gets a 'get'

Connects to a MQTT broker and publishes messages.

### Inputs

: payload (string | buffer) :  the payload of the message to publish.
: *topic* (string)          :  the MQTT topic to publish to.

### Outputs

1. Standard output
: payload (string) : the standard output of the command.

2. Standard error
: payload (string) : the standard error of the command.

### Details

`msg.payload` is used as the payload of the published message.
If it contains an Object it will be converted to a JSON string before being sent.
If it contains a binary Buffer the message will be published as-is.

The topic used can be configured in the node or, if left blank, can be set
`msg.topic`.

Likewise the QoS and retain values can be configured in the node or, if left
blank, set by `msg.qos` and `msg.retain` respectively.

### References

    - [Twitter API docs]() - full description of `msg.tweet` property
    - [GitHub]() - the nodes github repository
