# SignalR Integration Pack

Pack which allows triggers to be raised by SignalR

## Configuration

Copy the example configuration in [signalr.yaml.example](./signalr.yaml.example)
to `/opt/stackstorm/configs/signalr.yaml` and edit as required.

It must contain:

* ``hub_url`` - SignalR message hub URL
* ``hub_name`` -  The name of the hub for the sensor

**Note** : When modifying the configuration in `/opt/stackstorm/configs/` please
           remember to tell StackStorm to load these new values by running
           `st2ctl reload --register-configs`

## Actions
* `send_message` - Send a message to a hub

## Sensors

* `SignalRHubSensor` - Raises signalr.message\_received triggers for messages on the hub
