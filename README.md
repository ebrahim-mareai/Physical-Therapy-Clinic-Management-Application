# Physical Therapy Clinic Patient and Visit Management System

A Python desktop application for managing patient registration, waiting
queues, treatment plans, visit records, and patient history in a
physical therapy clinic. The application combines a Tkinter interface
with a local SQLite database and Excel import/export tools.

## Features

### Goal 1: Patient Registration & Queue Management

-   **Patient Registration**: Record patient details, including name,
    phone number, age, and payment status.
-   **Duplicate Detection**: Identify potential duplicate patients using
    normalized names and phone numbers.
-   **Waiting Queue**: View patients waiting for treatment and manage
    their queue status.
-   **Patient Updates**: Review and edit existing patient information.
-   **Return Visits**: Move a completed patient back into the queue when
    another visit is required.

### Goal 2: Treatment Plans & Visit Tracking

-   **Treatment Plans**: Set a prescribed number of visits for each
    patient.
-   **Ordered Treatment Steps**: Create treatment sequences with
    devices, durations, and instructions.
-   **Plan Editing**: Add, edit, remove, and reorder treatment steps
    before saving a plan.
-   **Treatment Workflow**: Display saved treatment steps for staff to
    follow and mark steps as completed.
-   **Visit Records**: Record completed visits and related notes.
-   **Patient History**: Review previous visits and see prescribed,
    completed, and remaining visit counts.

### Goal 3: Database & Excel Integration

-   **Local Database**: Store patient and treatment information in an
    SQLite database.
-   **Visit History**: Maintain records of individual visits and
    associated notes.
-   **Audit Records**: Keep records of selected changes and actions.
-   **Excel Export**: Export clinic data to a workbook containing
    `Patients`, `Visit History`, and `Recovery Steps` worksheets.
-   **Excel Import**: Import supported patient updates by matching
    patient IDs to existing records.

------------------------------------------------------------------------

## Tech Stack

-   **Language**: Python 3
-   **GUI Framework**: `tkinter` and `ttk`
-   **Database**: `sqlite3` (Local)
-   **Data Handling**: `pandas`
-   **Excel Support**: `openpyxl`
-   **Notebook Environment**: JupyterLab / IPython
-   **Architecture**: Modular notebook-based structure separating
    application startup, user interface, and business logic

------------------------------------------------------------------------

## Project Structure

The project is organized into three Jupyter Notebooks:

``` text
├── main.ipynb             # Application entry point and startup sequence
├── UserInterface.ipynb    # Tkinter interface, forms, queue, and treatment windows
└── BusinessLogic.ipynb    # Patient records, treatment plans, visits, database, and Excel operations
```

## Requirements

-   Python 3
-   Tkinter support
-   JupyterLab or another compatible Jupyter/IPython environment
-   `pandas`
-   `openpyxl`

Install the Python packages from a terminal:

``` bash
python -m pip install jupyterlab pandas openpyxl
```

Tkinter is included with many standard Python installations. On some
Linux distributions, it may need to be installed separately through the
operating system's package manager.

## Run the Application

1.  Clone or download this repository.

2.  Keep `main.ipynb`, `UserInterface.ipynb`, and `BusinessLogic.ipynb`
    in the same directory.

3.  Open a terminal in that directory and start JupyterLab:

    ``` bash
    jupyter lab
    ```

4.  Open `main.ipynb`.

5.  Run the notebook cells in order. The main notebook loads the
    business logic and user interface notebooks and starts the desktop
    application.

The application uses Tkinter windows, so it needs a graphical desktop
session. A headless notebook service may not be able to display the
interface.

## Data Storage

The application uses a local SQLite database named `clinic.db`, created
or updated in the application's working directory. Keep the database in
the directory used to run the application so the expected records can be
found.

Back up the database before testing imports or making changes to clinic
records.

## Privacy

Patient names, phone numbers, ages, payment status, treatment
instructions, and visit history may be sensitive. Do not upload real
patient records, exported workbooks, or a populated `clinic.db` file to
a public repository. Use synthetic data for demonstrations and testing.

## Current Scope

This repository contains the Jupyter notebooks for a local desktop
application. It does not, by itself, provide a hosted web application or
remote database service.

## License

No license file is currently included. Contact the repository owner
before reusing or redistributing the code.
