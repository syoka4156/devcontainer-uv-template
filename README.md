# Modern Python Environment Management with Dev Containers + uv

This repository provides a reproducible Python research environment using:

- Docker
- VS Code Dev Containers
- uv

The goal is to simplify environment setup while avoiding local dependency conflicts.

## Slides

The accompanying lecture slides are available on Speaker Deck:

- [Modern Python Environment for Engineering Researchers with Docker + uv](https://speakerdeck.com/shokazaki/modern-python-environment-for-engineering-researchers-with-docker-plus-uv)

## Prerequisites

Please install the following software before starting:

- Docker Desktop
- Visual Studio Code
- Dev Containers extension for VS Code

## Repository Structure

```text
project/
├── .devcontainer/
│   ├── devcontainer.json
│   └── Dockerfile
├── notebooks/
│   └── test.ipynb
├── src/
│   └── test.py
├── data/
│   └── .gitkeep
├── pyproject.toml
├── uv.lock
├── .gitignore
└── README.md
```

## Getting Started

### 1. Clone the Repository

```bash
git clone https://github.com/syoka4156/devcontainer-uv-template.git
```

### 2. Open in VS Code

Open the repository folder in VS Code.

### 3. Reopen in Container

When VS Code prompts:

```text
Reopen in Container
```

click it.

The container build may take several minutes during the first launch.

## Running Python Scripts

```bash
uv run python src/test.py
```

## Install a Package

```bash
uv add seaborn
```

## Using Jupyter Notebook

Open:

```text
notebooks/test.ipynb
```

in VS Code.

Select the Python kernel inside `.venv` if prompted.

## Useful Commands

### Sync dependencies

```bash
uv sync
```

### Add a package

```bash
uv add numpy
```

### Run Python

```bash
uv run python src/test.py
```
