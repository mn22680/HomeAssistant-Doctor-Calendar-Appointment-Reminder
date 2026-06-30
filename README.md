# Calendar Doctor Appointment Reminder

A Home Assistant automation blueprint that sends mobile alerts before matching
doctor, dentist, and other healthcare appointments.

[![Open your Home Assistant instance and import this blueprint](https://my.home-assistant.io/badges/blueprint_import.svg)](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https%3A%2F%2Fgithub.com%2Fmn22680%2FHomeAssistant-Doctor-Calendar-Appointment-Reminder%2Fblob%2Fmain%2Fcalendar_doctor_appointment_reminder.yaml)

## Calendar title format

Use a clear patient name inside brackets, followed by the appointment type:

```text
[Michael] Doctor
[Sarah] Dentist - Cleaning
[Alex] Orthodontist
```

Names are exact and case-sensitive. `Michael` matches `[Michael]`, but does not
match `[michael]`. Appointment types are case-insensitive and may be part of a
longer description, so `Dentist` matches `Dentist - Cleaning`.

## Features

- Select any Home Assistant calendar.
- Add multiple patient names with the blueprint editor's **Add** button.
- Add multiple appointment types without using comma-separated text.
- Choose a reminder time from 15 minutes to one week before the event.
- Alert one or more phones or tablets using the Home Assistant Companion App.
- Customize the notification title and message.
- Run optional extra actions after the mobile alerts.

Suggested appointment types include Doctor, Primary Care, Pediatrician,
Dentist, Orthodontist, Dermatologist, Eye Doctor, Optometrist, Ophthalmologist,
Cardiologist, Gynecologist, Physical Therapy, Chiropractor, Specialist, Lab
Work, Vaccination, and Telehealth.

## Installation

Use the **Import Blueprint** button above, or import this URL:

```text
https://github.com/mn22680/HomeAssistant-Doctor-Calendar-Appointment-Reminder/blob/main/calendar_doctor_appointment_reminder.yaml
```

Manual installation path:

```text
/config/blueprints/automation/mn22680/calendar_doctor_appointment_reminder.yaml
```

Then open **Settings → Automations & scenes → Blueprints**, find **Calendar
Doctor Appointment Reminder**, and select **Create automation**.

## Notes

- Create or edit test calendar events well before their reminder time because
  some calendar integrations poll periodically.
- The alert devices must be registered through the Home Assistant Companion App.
- Each event should have one patient name inside the first pair of brackets.
- The automation runs only when both a configured name and appointment type match.

## Suggested next improvements

- A second reminder, such as one day before and again two hours before.
- Optional actionable buttons such as **Open Calendar** or **Acknowledge**.
- A configurable fallback alert when a title is missing brackets.
- Optional location and description details in the message.
