# J1 Pro – app online content

The J1 Pro Android app (2.4 and later) reads these files when the phone is online.
Changes here reach every user **without a Play Store update**.

| File | Used for |
|---|---|
| `version.json` | "New version available" banner on Home and *Check for updates* in About. `latest_code` must equal the newest app version code on Google Play. `important_below` turns on the pop-up for an important fix. |
| `gov.json` | Government Exams: corrections to dates, fees, links, new exams, extra practice questions. |
| `syllabus.json` | Engineering Syllabus: new or corrected subjects (full subject data per subject code). |

Rules
- Every change to `gov.json` / `syllabus.json` must **increase `ver`** (format `yyyymmddNN`), otherwise the app ignores it.
- `app_min` = the lowest app version code that understands the file (53 = app 2.4).
- Keep the JSON valid – a broken file is ignored and users keep the built-in content.
- Prepared and checked by Claude before publishing; please do not edit by hand.
