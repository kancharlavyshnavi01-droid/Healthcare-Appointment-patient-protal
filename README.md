# Healthcare Appointment & Patient Portal

A responsive web application for registering patients, booking doctor appointments, and viewing appointment and health information. Built with **HTML5**, **CSS3** and **Bootstrap 5**.

## Features

- **Navigation bar:** Home, Patient Registration, Appointments, Health Information, Services, Technologies (fixed and collapsible on mobile)
- **Patient Registration form** (Bootstrap card) with 12 fields:
  name, email, mobile number, date of birth, gender, blood group, department, doctor, appointment date, appointment time, address, symptoms
- **HTML5 validation:** `required`, `pattern`, `minlength`, `min`/`max`, and input types `email`, `tel`, `date`, `time`
  - Appointment date cannot be in the past
  - Date of birth cannot be in the future
  - Appointment time limited to 09:00-17:00
  - Mobile number must be 10 digits
- **Dependent dropdown:** the Doctor list changes with the selected Department
- **Appointments table:** ID, patient name, department, doctor, date, time, status
- **Health Information cards:** blood group, department, doctor, appointment date and time, symptoms, status
- **Services** and **Technologies** sections
- Register and Reset buttons

## Technologies

| Technology | Purpose |
|---|---|
| HTML5 | Structure, forms, built-in validation |
| CSS3 | Custom styling and gradients |
| Bootstrap 5.3 | Responsive grid, navbar, cards, tables, forms, badges |
| JavaScript (minimal) | Dependent doctor dropdown and adding new records |

## Project Structure

```
healthcare-portal/
├── healthcare.html   # complete application (HTML, CSS and JS in one file)
└── README.md
```

## How to Run

1. Download `healthcare.html`.
2. Double-click it to open in any modern browser.
3. An internet connection is needed because Bootstrap is loaded from a CDN.

No installation or build step is required.

## How It Works

1. The user fills in the registration form. The browser checks each field using HTML5 validation.
2. On a valid submit, a new appointment ID (e.g. `APT-1003`) is generated with a **Pending** status.
3. The record is added to the **Appointments** table and to the **Health Information** cards.
4. **Reset** clears the form and the doctor dropdown.

## Customisation

- **Departments and doctors:** edit the `<option>` list in the Department select and the `doctors` object in the script.
- **Sample data:** edit the two sample rows in the Appointments table and the two cards under Health Information.
- **Appointment hours:** change the `min` and `max` attributes on the time input.
- **Without JavaScript:** delete the `<script>` block at the bottom. Validation still works, but list the doctors directly in the HTML.

## Limitations

- Data is stored in memory only and is lost when the page is refreshed.
- There is no login system or backend database.

## Future Enhancements

- User login and patient dashboard
- Backend and database storage
- Appointment cancellation and rescheduling
- Email or SMS reminders
- Downloadable medical reports

## License

For educational use.
