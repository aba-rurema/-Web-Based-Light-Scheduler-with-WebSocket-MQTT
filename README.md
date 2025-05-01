# -Web-Based-Light-Scheduler-with-WebSocket-MQTT
A web-based IoT scheduler that lets users set ON/OFF times for a light. The browser sends the schedule via WebSocket to a Python server, which publishes it to MQTT. A subscriber reads it and sends commands to Arduino via serial to control the light at the scheduled times.
# Web-Based Light Scheduler

## Overview
A simple IoT project to schedule a light using a web interface, WebSocket, MQTT, and Arduino.

## Tech Stack
- HTML, CSS, JS
- Python (websockets, paho-mqtt, pyserial)
- mosquitto_pub/sub
- Arduino UNO

## How it Works
1. User schedules ON and OFF time via browser.
2. Schedule sent via WebSocket to Python server.
3. Server publishes schedule to MQTT broker.
4. Python subscriber receives schedule and communicates with Arduino.
5. Arduino triggers relay based on received commands.

## Run Instructions
1. Start the WebSocket server:
    ```bash
    python3 backend/server.py
    ```
2. Start the MQTT subscriber:
    ```bash
    python3 subscriber/subscriber.py
    ```
3. Open `frontend/index.html` in your browser.

## Demo
![Demo GIF](demo.gif)

---

