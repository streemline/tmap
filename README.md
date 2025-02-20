# Telegram  Map

Telegram Nearby Map uses OpenStreetMap and the official Telegram library to find the position of nearby users.

<img src=".github/telegram-nearby-map-small.png" alt="Telegram Nearby Map Screenshot">  

## How does it work?
Every 25 seconds all nearby users will be received with [TDLib](https://core.telegram.org/tdlib) from Telegram. This includes the distance of every nearby user to "my" location. With three distances from three different points, it is possible to calculate the position of the nearby user.

This only finds Telegram users which have activated the nearby feature. Per default it is deactivated.

## Installation

Requirements: node.js and an Telegram account

1. Create an API key for your Telegram account [here](https://my.telegram.org)
2. Download the repository
3. Create config.js (see config.example.js) and put your Telegram API credentials in it
4. Install all dependencies: npm install
5. Start the app: npm start
6. Look carefully at the output: you will need to confirm your Telegram login
7. Go to http://localhost:3000 and have fun

## Dependencies
To avoid that you have to build TDLib yourself (https://github.com/tdlib/td#building), I added [tdlib.native](https://github.com/ForNeVeR/tdlib.native/releases) in the lib/tdlib folder. Please note that this is an external dependency that has not been fully reviewed by me!

## Changelog

### 2021-11-13
- Added [tdlib.native](https://github.com/ForNeVeR/tdlib.native/releases) for Linux (now it works in GitHub Codespaces)
- Updated all dependencies
- Bugfixes
