# Intelligent Vending Machine Project (ivm-bd)

This repository contains the "Intelligent Vending Machine Project" (ivm-bd), a project created to manage and simulate an intelligent vending machine using various technologies. Below you'll find a detailed explanation of the project's structure, functionality, and purpose.

---

## Table of Contents
- [Overview](#overview)
- [Project Structure](#project-structure)
- [Dependencies](#dependencies)
- [Makefile Targets](#makefile-targets)
- [Documents](#documents)
- [How To Run](#how-to-run)


---

## Overview

This project is focused on building an intelligent vending machine system. The repository is organized into multiple subdirectories and files that cover:
- Source code for the vending machine's functionalities.
- Database scripts (written in PLpgSQL) for managing the backend.
- Documentation for different project deliverables.

The main languages used in this project are:
- **Python** (54.3%): Backend logic for the vending machine.
- **HTML** (35.8%): Frontend interface for interacting with the vending machine.
- **PLpgSQL** (6.5%): Database scripts for handling data storage and retrieval.
- **Makefile** (2.7%): Build automation for generating project deliverables.
- **CSS** (0.7%): Styling for the frontend interface.

---

## Project Structure

The repository is structured as follows:

```
ivm-bd/
├── docs/                # Documentation and deliverables
│   ├── e1/             # Deliverable 1 documents
│   ├── e2/             # Deliverable 2 documents
│   ├── e3/             # Deliverable 3 documents
│   ├── enunciado/      # Problem statements and guidelines
├── src/                 # Source code for the project
│   ├── populate/       # Scripts for populating the database
├── Makefile             # Automation of tasks like building and zipping deliverables
```

---

## Dependencies

The project relies on the following tools:
- **LaTeX**: Used for compiling `.tex` files into `.pdf` documents.
- **zip**: For creating compressed deliverables.
- **PostgreSQL**: Backend database management system.

Ensure these tools are installed before running the project.

---

## Makefile Targets

The `Makefile` automates various tasks in the project. Below are the available targets:

### `all`
- Default target: Runs the `zip` target.

### `1`
- Generates the first deliverable:
  - Compiles `cover.tex` and merges it with `modelo.pdf` into `delivery-01-64.pdf`.
  - Location: `docs/e1`.

### `2`
- Generates the second deliverable:
  - Compiles `relatorio.tex` into `delivery-02-64.pdf`.
  - Location: `docs/e2`.

### `3`
- Generates the third deliverable:
  - Compiles `relatorio.tex` into `64-relatorio.pdf`.
  - Location: `docs/e3`.

### `clean`
- Cleans up generated files:
  - Removes all `.aux`, `.log`, `.nav`, `.out`, `.snm`, `.toc` files.
  - Deletes compiled PDFs and zip files.

### `zip`
- Creates a zip archive of the third deliverable:
  - Includes `64-relatorio.pdf` and SQL files from the `src/` directory.

---

## Documents

### Deliverable 1 (`docs/e1`)
- **`cover.tex`**: LaTeX file for the cover page of Deliverable 1.
- **`modelo.pdf`**: A PDF file used as part of Deliverable 1.
- **Output**: `delivery-01-64.pdf`.

### Deliverable 2 (`docs/e2`)
- **`relatorio.tex`**: LaTeX file containing the report for Deliverable 2.
- **Output**: `delivery-02-64.pdf`.

### Deliverable 3 (`docs/e3`)
- **`relatorio.tex`**: LaTeX file containing the report for Deliverable 3.
- **Output**: `64-relatorio.pdf`.

---

## How to Run

1. **Install dependencies**:
   - Install LaTeX for compiling `.tex` files.
   - Install `zip` for archiving files.
   - Ensure PostgreSQL is set up for database scripts.

2. **Generate Deliverables**:
   - Run `make 1` to generate Deliverable 1.
   - Run `make 2` to generate Deliverable 2.
   - Run `make 3` to generate Deliverable 3.

3. **Create a Zip Archive**:
   - Run `make zip` to generate a zip archive of the third deliverable.

4. **Clean Up**:
   - Run `make clean` to remove temporary and generated files.

---
