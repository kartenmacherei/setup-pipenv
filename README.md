# setup-pipenv

A GitHub action to install python and setup + activate a virtual environment with pipenv.
Other than existing pipenv GitHub actions, the virtual environment is activated after it is set up.
So the rest of the workflow doesn't need to know that pipenv was used in creating the environment.

## Inputs

- `python-version`: The Python version to use (e.g., `3.9`)
- `additional-dependencies`: (optional) A list of python libraries to be installed via pip
after setting up the virtual environment with the dependencies from `Pipfile.lock`.
This might be useful if there are certain dependencies only for the workflow
that are not needed for the rest of the project.
