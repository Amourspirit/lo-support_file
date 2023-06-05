# Pre-configured virtual environments for Windows

This directory contains pre-configured virtual environments for LibreOffice on Windows.

While it is possible to create a virtual environment for LibreOffice on Windows, it is not a straight forward process.
Normally it involves installing a python environment that matches the python environment in LibreOffice and then creating a virtual environment using that python environment, and then modifing the virtual environment to work with LibreOffice.
The virtual environments in this directory are pre-configured to work with LibreOffice on Windows.

## Requirements

LibreOffice that uses python 3.8 or later is required to use the virtual environments.

Python version can be checked by running the following command in PowerShell.

```powershell
>&"C:\Program Files\LibreOffice\program\python.exe" --version
Python 3.8.16
```

## How to use

1. Create a directory for your project environment.
2. Download the virtual environment you want to use.
3. Extract the archive to the directory you created.

### Extracting the archive using PowerShell

Extract the archive to the current directory.

```powershell
Expand-Archive -Path <path-to-archive> -DestinationPath .
```

## Available virtual environments

Virtual Environment for LibreOffice using Python 3.8.

- File Name: [libre_office_python38_venv_v1.zip](./libre_office_python38_venv_v1.zip)
- MD5: `E5EA1B11CFA01D4F9AEB0BF2DF8506D3`
- SHA1: `1458E4ADED0B6B30D571524030EBFB6C52C70436`
- SHA-256: `3D3CC28BBB93214866DD90602D0F0F434DBBD7EDCA6650EECF40CC3AC035C649`

## Verify hashes in Windows using PowerShell

```powershell
Get-FileHash -Path <path-to-file> -Algorithm MD5
Get-FileHash -Path <path-to-file> -Algorithm SHA1
Get-FileHash -Path <path-to-file> -Algorithm SHA256
```

## Virtual Environment contents.

The virtual environment contains the following:

- pip
- setuptools
- wheel
- oooenv

## Activating Virtual Environment

The virtual environment can be activated by running the following command in PowerShell from your project directory.

```powershell
.\.venv\Scripts\activate.ps1
```

Once the virtual environment is activated, you can use pip to install packages.

For Instance:

```powershell
pip install ooo-dev-tools
```

## Post Installation

After Activating the virtual environment the following commands should be run to ensure the virtual environment is configured correctly.

Ensure pip is up to date.

```powershell
pip install --upgrade pip
```

[oooenv](https://pypi.org/project/oooenv/) is a tool that amongst other things allows you to update the virtual environment to match the python environment in LibreOffice.

Ensure `oooenv` is up to date.

```powershell
pip install --upgrade oooenv
```

Run `oooenv` update command to ensure the virtual environment is configured correctly.

```powershell
oooenv update --update
```

## Other Resources

- [OOO Development Tools (OooDev)](https://python-ooo-dev-tools.readthedocs.io/en/latest/index.html)
- [Poetry](https://python-poetry.org/)
