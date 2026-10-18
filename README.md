# Physical Therapy Clinic Management Application

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

## Current Scope

This repository contains the Jupyter notebooks for a local desktop
application. It does not, by itself, provide a hosted web application or
remote database service.
