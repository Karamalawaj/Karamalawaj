# Bright Eyes

**Ophthalmology clinic application showcase · 2024**

> This page presents the implemented product workflow without requiring the full source repository to remain public.

## Overview

Bright Eyes is a single-clinic ophthalmology application prototype built with separate patient and clinic/doctor workflows.

The project focuses on appointment scheduling, registered-patient management, structured eye examination records, and patient access to read-only medical report data.

## Implemented workflows

### Patient experience
- email/password account flow;
- patient profile creation;
- clinic-opened appointment dates;
- appointment time selection and conflict prevention;
- patient appointment tracking;
- read-only access to structured eye examination results.

### Clinic / doctor experience
- controlled doctor access path;
- registered-patient management;
- clinic scheduling and appointment administration;
- structured right/left-eye examination fields;
- editing clinical values that patients can later review.

## Structured eye report

The application models ophthalmology values for both eyes, including fields such as:

- sphere (`Sph`);
- cylinder (`Cyl`);
- axis (`Ax`).

Doctor-side values can be edited while the patient-facing report remains read-only.

## Appointment safeguards

Appointment creation is tied to the patient's Firebase UID. Existing appointments are checked to prevent overlapping reservations within the configured booking interval, while compatibility is retained for older records created before UID-based linking was introduced.

## Architecture and stack

**Flutter · Dart · GetX · Firebase Authentication · Cloud Firestore**

The application uses GetX for controllers and navigation, with Firebase providing authentication and persistent application data.

## Security posture

No clinic access password is committed to the repository. The demo access value is provided at runtime through environment configuration, while production authorization should be enforced server-side rather than trusted to a mobile-client check.

Private keys, service-account credentials, local environment files, and similar sensitive configuration are excluded from version control.

## Source visibility

The source repository may be kept **private** while this public showcase remains available to recruiters and technical reviewers.

This preserves the ability to demonstrate the project without exposing the full implementation or internal configuration.

---

**Designed and developed by Karam Alawaj.**
