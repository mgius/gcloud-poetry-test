This project fails to run in app engine when pyproject.toml exists.

The project cannot import the "six" module.  This is despite the fact that
requirements.txt contains an explicit installation of the "six" library and
"six" is a dependency of one of our poetry managed explicit dependencies.

 - This project successfully runs when pyproject.toml is deleted and deployed.
 - This project fails to run with an import error when pyproject.toml is present.

The presence or absence of requirements.txt is irrelevant when pyproject.toml
is present.  It always fails to run.


Deployment: gcloud app deploy.  us-central.  Default settings for everything.
