# mule-publisher

A mule project to act as a receiver for messaged posted at its address.

The messages are transformed from Byte[] to String and published into a JMS topic at an ActiveMQ instance.

This is to act as a fire-and-forget action, but for the peace of mind of the sender a success msg is returned.

A second flow is a subscription to the same topic and is there to check if the msg actually arrived at the ActiveMQ instance and can be subscripted to.
