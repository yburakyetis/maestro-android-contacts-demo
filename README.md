# Maestro Mobile Automation Demo

This repository contains a small **proof-of-concept mobile automation project** built to explore and evaluate [Maestro](https://maestro.mobile.dev/) as a mobile UI testing tool.

The goal of the project is to demonstrate a **clear, readable, and reusable Maestro flow** for a basic Android user scenario.

---

## Purpose

As a **Backend Engineer**, I wanted to explore mobile test automation from a practical standpoint and evaluate how well Maestro fits into modern engineering workflows.

The main goals of this project are to:

- Gain hands-on experience with **Maestro’s YAML-based DSL**
- Evaluate the **readability and maintainability** of Maestro flows
- Understand how effectively Maestro supports **reusable test components** through subflows

This project is intentionally kept **simple and deterministic**, prioritizing clarity and structure over exhaustive coverage.

---

## Scenario Covered

The automated test performs the following steps on the **Android Contacts** app:

1. Launches the app with a clean state
2. Initiates the "Create new contact" flow
3. Enters:
   - First Name
   - Last Name
   - Phone Number
4. Saves the contact
5. Asserts that the saved contact details are visible on screen

---

## Prerequisites

- **Maestro**  
  Follow the official installation guide:  
  https://maestro.mobile.dev/getting-started/installing-maestro

- **Android Emulator**  
  Any running AOSP / Google Play emulator.

- **Application Under Test**  
  Stock Android Contacts app:  
  `com.android.contacts` (pre-installed on most emulators)

---

## Project Structure

- `flow.yaml`: The main test suite entry point.
- `subflows/`: Reusable test components.
    - `launch_app.yaml`: Handles app launch and state clearing.
    - `create_contact.yaml`: Performs the "Create Contact" user flow.

## Running the Tests

1. **Start your Android Emulator**.
2. **Run the test suite**:

```bash
maestro test flow.yaml
```

## Scenario

The test performs the following steps:
1. Launches the Contacts app (clearing previous state).
2. Taps "Create new contact".
3. Enters First Name, Last Name, and Phone Number.
4. Saves the contact.
5. Asserts that the saved contact details are visible on the screen.
