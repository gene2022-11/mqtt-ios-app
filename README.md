# MQTT Control iOS App

A self-contained iOS application for controlling MQTT devices. Built with Cordova.

## Features

- ✅ Fully self-contained (no web server needed)
- ✅ MQTT WebSocket communication
- ✅ Persistent settings using localStorage
- ✅ Works offline (except for MQTT connection)
- ✅ Native iOS feel

## Building Locally (requires macOS)

```bash
# Install dependencies
npm install -g cordova

# Build for iOS
cordova build ios

# Open in Xcode
cordova run ios
```

## Building with GitHub Actions (No Mac Required)

1. Push this repo to GitHub
2. Go to Actions tab
3. Click "Build iOS App" workflow
4. Click "Run workflow"
5. Download the artifact when complete

## Setup Instructions

1. Install the app on your iPhone
2. Open the app
3. Tap the ⚙️ settings icon
4. Configure:
   - Your phone number
   - MQTT broker address
   - Port (usually 8884 for WSS)
   - Topics for command/status
5. Tap "Save Settings"
6. Tap "Connect"

## MQTT Configuration

The app connects to MQTT brokers via WebSocket (WS/WSS).

Example brokers:
- `broker.hivemq.com` (port 8884 for WSS)
- `test.mosquitto.org` (port 8081 for WS)

Make sure your broker supports WebSocket connections!

## Troubleshooting

**Connection fails:**
- Check broker URL and port
- Ensure broker supports WebSocket
- Verify SSL/TLS setting matches broker

**App won't build:**
- Make sure you have the latest Cordova
- Try: `cordova clean`
- Remove and re-add platform: `cordova platform rm ios && cordova platform add ios`

## License

MIT
