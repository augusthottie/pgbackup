# pgbackup

## Overview
`pgbackup` is a simple command-line tool for backing up remote PostgreSQL databases either locally or to AWS S3. This tool is designed to streamline the process of creating and storing backups, making it easy to safeguard your data.

## Features
- Backup a PostgreSQL database using `pg_dump`.
- Store backups locally or upload them directly to AWS S3.

## Usage
To use `pgbackup`, pass a complete database URL, along with the desired storage driver (`local` or `s3`) and the destination for the backup.

### Backing up to AWS S3
```bash
$ pgbackup postgres://bob@example.com:5432/db_one --driver s3 backups
```

### Backing up locally
```bash
$ pgbackup postgres://bob@example.com:5432/db_one --driver local /var/local/db_one/backups
```

## Installation

### From Source
To install `pgbackup` from source, follow these steps:

1. Clone the repository:
    ```bash
    git clone https://github.com/AugustHottie/pgbackup.git
    ```
2. Navigate into the project directory:
    ```bash
    cd pgbackup
    ```
3. Install the package using `pip`:
    ```bash
    pip install --user -e .
    ```

This will install the package in editable mode, making it easier to develop and test changes.

## Project Structure and Setup
For Python projects intended for distribution as a package, the most important file is `setup.py`. This file is used by `pip` and `setuptools` to manage installation and dependencies.

### Setting Up the Project Directory
Ensure that the following steps are taken when working with this project:
- The `setup.py` file defines how the package is installed.
- All necessary dependencies should be listed in the `Pipfile` for easy installation.

## Development Guide

### Prerequisites
Before starting development, make sure you have the following installed:
- Python (preferably version 3.8+)
- `pip`
- `pipenv` (for managing virtual environments and dependencies)

### Development Setup
To start developing with `pgbackup`:

1. Clone the repository:
    ```bash
    git clone https://github.com/AugustHottie/pgbackup.git
    ```
2. Navigate into the project directory:
    ```bash
    cd pgbackup
    ```
3. Activate the virtual environment:
    ```bash
    pipenv shell
    ```
4. Install the project dependencies:
    ```bash
    pipenv install
    ```

You're now ready to start developing!

## Contributing
If you'd like to contribute to this project, please follow these guidelines:
1. Fork the repository.
2. Create a new branch for your feature or bugfix.
3. Submit a pull request with a detailed description of the changes.

---