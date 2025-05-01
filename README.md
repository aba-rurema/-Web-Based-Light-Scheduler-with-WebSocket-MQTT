# -Web-Based-Light-Scheduler-with-WebSocket-MQTT
A web-based IoT scheduler that lets users set ON/OFF times for a light. The browser sends the schedule via WebSocket to a Python server, which publishes it to MQTT. A subscriber reads it and sends commands to Arduino via serial to control the light at the scheduled times.
