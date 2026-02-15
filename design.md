# Design Document: Patient Queue Management System

## Overview

The Patient Queue Management System is a web-based healthcare workflow automation tool that streamlines patient appointments through intelligent token generation, real-time queue management, and location-aware scheduling. The system integrates map visualization and navigation features to provide patients with optimal departure times and turn-by-turn directions to the hospital.

The system serves three primary user groups:
- **Patients**: Book appointments, receive tokens, view wait times, and navigate to the hospital
- **Doctors**: View and manage their patient queues
- **Hospital Administrators**: Configure schedules, monitor system-wide queue status

**Key Design Principles:**
- Real-time updates for queue status and travel times
- Location-aware scheduling with traffic consideration
- Clear separation between patient, doctor, and admin interfaces
- Synthetic data only with prominent disclaimers
- Mobile-first responsive design for patient interface

## Architecture

The system follows a three-tier architecture with clear separation of concerns.

**Architecture Decisions:**
1. **RESTful API**: Stateless API design for scalability
2. **Event-driven updates**: WebSocket connections for real-time queue and travel time updates
3. **Third-party map integration**: Use established mapping services (Google Maps, Mapbox) rather than building from scratch
4. **Token-based authentication**: JWT tokens for secure, stateless authentication
5. **In-memory caching**: Redis for frequently accessed data (active queues, wait times)

## Components and Interfaces

The design document includes detailed interfaces for:
- Token Generator
- Queue Manager
- Travel Time Estimator
- Departure Calculator
- Map Interface
- Notification Service
- Authentication Service

## Data Models

Core data models include:
- Patient
- Doctor
- Appointment
- GeoLocation
- Hospital

## Correctness Properties

The system has 50 correctness properties covering all testable requirements. Key properties include:

- Token uniqueness and generation
- Queue ordering and progression
- Travel time estimation and departure calculation
- Map rendering and navigation
- Authentication and authorization
- Data persistence and retrieval

## Testing Strategy

- **Unit tests**: Specific examples, edge cases, error conditions
- **Property tests**: Universal properties across all inputs using fast-check library
- Minimum 100 iterations per property test
- Both approaches are complementary and necessary

For full design details, see: ~/.kiro/specs/patient-queue-management/design.md
