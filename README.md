# Patient Queue Management System

A healthcare workflow automation tool that helps patients book appointments online, get smart departure times based on their location and traffic, and navigate to the hospital with real-time directions.

## ⚠️ Disclaimer

This system uses **synthetic data only** for demonstration purposes. It does NOT provide medical advice. Scheduling times are estimates and subject to traffic and other external factors.

## Features

- **Online Token Generation** - Book appointments without visiting the hospital
- **Smart Departure Times** - Know exactly when to leave based on your location and traffic
- **Google Maps Integration** - Turn-by-turn navigation with real-time traffic updates
- **Real-Time Queue Updates** - See your wait time and position in the queue
- **Multi-Channel Notifications** - Get updates via email, SMS, or in-app
- **Multiple Transport Modes** - Driving, public transit, or walking directions

## Quick Start

```bash
# Install dependencies
npm install

# Set up environment
cp .env.example .env
# Edit .env with your API keys

# Run migrations
npm run migrate

# Start the server
npm run dev
```

## Requirements

- Node.js 18+
- PostgreSQL 14+ with PostGIS
- Redis 7+
- Google Maps API key

## Tech Stack

- **Frontend**: React, TypeScript, Google Maps API
- **Backend**: Node.js, Express
- **Database**: PostgreSQL with PostGIS
- **Cache**: Redis
- **Real-time**: WebSocket
- **Auth**: JWT

## Documentation

- [Requirements](requirements.md) - System requirements
- [Design](~/.kiro/specs/patient-queue-management/design.md) - Technical design

## Testing

```bash
# Run unit tests
npm test

# Run property-based tests
npm run test:properties
```

## License

MIT License - see [LICENSE](LICENSE) file

## Contributing

Pull requests are welcome. For major changes, please open an issue first.

---

**Note**: This is a demonstration project. Always consult healthcare professionals for medical advice.
