# NGit - Nostr Git Repository Event Viewer

A real-time web application that displays Git repository announcements from the Nostr network using NIP-34 events.

## Overview

NGit connects to multiple Nostr relays and listens for Git repository events (kind 30617) to provide a live feed of repository announcements. The application displays repository information including names, descriptions, URLs, and maintainer information in an elegant, responsive interface.

## Features

- **Real-time Updates**: Connects to multiple Nostr relays for live repository events
- **Multi-relay Support**: Automatically connects to 9 popular Nostr relays with failover
- **Repository Information**: Displays repository names, descriptions, URLs, and maintainer data
- **Responsive Design**: Mobile-friendly interface with modern styling
- **Auto-reconnection**: Automatically reconnects to relays on connection loss
- **Event Deduplication**: Prevents duplicate events from appearing

## How It Works

1. **Relay Connection**: Connects to multiple Nostr relays simultaneously
2. **Event Subscription**: Subscribes to NIP-34 Git repository events (kind 30617)
3. **Data Parsing**: Extracts repository information from event tags and content
4. **Real-time Display**: Shows events in chronological order with live updates

## Supported Relays

- wss://relay.nostr.net/
- wss://nos.lol/
- wss://relay.damus.io/
- wss://nostr.wine/
- wss://relay.snort.social/
- wss://nostr.mom/
- wss://relay.nostr.band/
- wss://purplepag.es/
- wss://offchain.pub/

## Usage

Simply open `index.html` in a web browser. The application will automatically:
1. Connect to Nostr relays
2. Subscribe to Git repository events
3. Display live repository announcements

No installation or build process required - it's a single HTML file with embedded JavaScript.

## Technical Details

- **Frontend**: Preact with HTM for JSX-like syntax
- **Styling**: Custom CSS with CSS variables for theming
- **WebSocket**: Native WebSocket API for Nostr relay connections
- **Protocol**: Implements NIP-34 for Git repository events

## Event Structure

The application listens for Nostr events with:
- **Kind**: 30617 (NIP-34 Git repository events)
- **Tags**: Parsed for repository metadata (name, URL, maintainers, etc.)
- **Content**: Repository description or name

## License

MIT License - see LICENSE file for details

## Contributing

This project is part of the play-grounds organization. Feel free to submit issues or pull requests.
