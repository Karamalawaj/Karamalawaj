# HealHub

**Healthcare application showcase · 2025**

> This page is intentionally portfolio-focused. It explains the product behavior and engineering scope without requiring the application source code to remain public.

## Overview

HealHub is a role-based healthcare application prototype built around separate patient and doctor workflows.

The application combines authentication, doctor profiles and schedules, appointment booking and lifecycle management, digital prescriptions, ratings, community interactions, notifications, and media handling in one Flutter/Firebase system.

## Implemented workflows

### Patient flow
- account registration and authentication;
- patient profile setup;
- doctor discovery and doctor details;
- schedule-aware appointment booking;
- appointment history and status tracking;
- prescription viewing;
- doctor ratings after completed appointments;
- community posts, likes, comments, and media;
- notification center.

### Doctor flow
- doctor account/profile setup;
- specialty, clinic, bio, and weekly working-hour configuration;
- appointment review and status transitions;
- confirmed appointment management;
- prescription creation;
- community participation and notifications.

## Scheduling model

Doctor working hours are used to generate appointment availability, with booking logic organized around 30-minute slots and existing reservations.

Appointments move through lifecycle states such as pending, confirmed, completed, and cancelled.

## Architecture and stack

**Flutter · Dart · GetX · Firebase Authentication · Cloud Firestore · Firebase Messaging · Cloudinary integration**

GetX is used for routing, dependency injection, controllers, and reactive state. Firebase handles authentication and application data, while external media handling is separated from the database layer.

## Security posture

The public portfolio intentionally avoids publishing server credentials or private service secrets.

Client-side Firebase configuration is not treated as an authorization boundary. Real protection must be enforced through Firebase Authentication, Firestore/Storage security rules, App Check where appropriate, and restricted provider credentials.

Client-side media uploads use an unsigned preset model; provider API secrets must remain server-side.

## Source visibility

The source repository may be kept **private** while this showcase remains public.

That approach allows the project to be reviewed from a product and architecture perspective without exposing the full implementation, internal configuration, or sensitive operational details.

---

**Designed and developed by Karam Alawaj.**
