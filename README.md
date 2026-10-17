# Physical Therapy Clinic Patient and Visit Management

A Python desktop application for managing patient registration, the
waiting queue, treatment plans, visit records, and patient history in a
physical therapy clinic.

## Overview

The application uses a Tkinter graphical interface and a local SQLite
database. Clinic staff can register patients, review the waiting queue,
prepare ordered treatment plans, record completed visits, review visit
history, and exchange selected clinic records through Excel files.

The project is organized into three Jupyter notebooks.

## Project Structure

``` text
.
├── main.ipynb
├── UserInterface.ipynb
└── BusinessLogic.ipynb
```

-   **`main.ipynb`** starts the application, loads the other notebooks,
    connects the interface controls to their handlers, loads the patient
    queue, and starts the desktop window.
-   **`UserInterface.ipynb`** defines the Tkinter windows, forms,
    tables, buttons, treatment-plan editor, visit-execution window, and
    patient-history views.
-   **`BusinessLogic.ipynb`** manages SQLite operations, patient
    records, duplicate matching, treatment steps, visit counts, history,
    audit entries, and Excel import/export.

Keep all three notebooks in the same directory and retain these
filenames. The launcher refers to `BusinessLogic.ipynb` and
`UserInterface.ipynb` by name.

## Features

### Patient records and waiting queue

-   Register patients with a name, phone number, age, and payment
    status.
-   View patients waiting for treatment.
-   Identify possible duplicate records using normalized names and phone
    numbers.
-   Review matching records before deciding whether to use an existing
    patient or enter a different patient.
-   Edit patient details and return a completed patient to the waiting
    queue when another visit is needed.

### Treatment plans

-   Set the number of visits prescribed for a patient.
-   Create an ordered list of treatment steps.
-   Choose from the available device presets or configure a step
    manually.
-   Record the duration and separate instructions for each step.
-   Edit, remove, and reorder steps before saving the plan.

### Visit execution and history

-   Display the saved treatment steps for the nurse to follow.
-   Mark treatment steps as completed.
-   Record completed visits and visit notes.
-   Display prescribed, attended, and remaining visit counts.
-   Review a patient's visit history and related treatment information.
-   Maintain audit entries for selected record changes and actions.

### Excel import and export

-   Export clinic information to an Excel workbook.
-   The export includes `Patients`, `Visit History`, and
    `Recovery Steps` worksheets.
-   Import supported patient updates from an Excel workbook using
    patient IDs to identify existing records.

## Requirements

-   Python 3 with Tkinter support
-   JupyterLab or another IPython/Jupyter environment
-   `pandas`
-   `openpyxl`

Install the Python packages from a terminal:

``` bash
python -m pip install jupyterlab pandas openpyxl
```

Tkinter is included with many standard Python installations. On some
Linux distributions, it must be installed separately through the
operating system's package manager.

## Run the Application

1.  Download or clone this repository.

2.  Confirm that `main.ipynb`, `UserInterface.ipynb`, and
    `BusinessLogic.ipynb` are in the same directory.

3.  Open a terminal in that directory and start JupyterLab:

    ``` bash
    jupyter lab
    ```

4.  Open `main.ipynb` in JupyterLab.

5.  Run the notebook cells in order. The launcher loads the
    business-logic and user-interface notebooks, then opens the clinic
    desktop window.

The application requires a graphical desktop session. A headless
notebook service or a platform without Tkinter window support will not
display the interface as intended.

## Local Database

The application stores its data in a SQLite database named `clinic.db`,
created or updated in the application's working directory.

The database contains patient records and related treatment and visit
information. Back up `clinic.db` before making changes to the
environment, importing data, or testing database updates. Keep the
database in the same working directory used to run the application so
that the expected records are loaded.

## Data and Privacy

Patient names, phone numbers, ages, payment status, treatment
instructions, and visit history may be sensitive information. Do not
commit real patient records, exported workbooks, or a populated
`clinic.db` file to a public repository. Use synthetic data for
demonstrations and testing, and store real clinic records only in an
appropriately controlled environment.

The current project is a local desktop application. The notebooks do not
provide a hosted web service, remote database synchronization, or
login-based user authentication. Access to the computer and its files
should therefore be managed carefully.

## Current Scope

This repository contains the application notebooks. It does not include
a bundled sample database or a packaged desktop installer. Excel
import/export depends on the installed Python packages and compatible
workbook files.

## License

No license file is currently included. Contact the repository owner
before reusing or redistributing the code.
