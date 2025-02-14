# zigbee2mqtt-standalone-quickstart

A minimal zigbee2mqtt setup Dockerized with Compose to quickly deploy and manage Zigbee devices from a local host. Start managing Zigbee devices in a few seconds without searching for additional dependencies.

## Requirements

- Docker CE https://docs.docker.com/engine/install

Note one needs exactly Docker CE, not Docker Desktop. Docker Desktop does not support mounting devices so it is not possible to mount a Zigbee adapter there https://forums.docker.com/t/error-response-from-daemon-error-gathering-device-information-while-adding-custom-device/132143

## Startup

With Docker installed it takes just a few seconds to start this zigbee2mqtt setup:
1. connect a Zigbee adapter to your host
2. find a path to a Zigbee adapter using a command `ls -l /dev/serial/by-id`
3. cd into the repo root dir
4. modify `devices` section (path before ":") in a Compose file to point to a Zigbee adapter in a local host
5. deploy the app
```
docker compose up
```

Once deployed a frontend will be accessible on http://localhost:8080. Now you can pair and control your Zigbee devices
