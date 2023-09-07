# depthai-windows-issue-demo

This repo demonstrates issue I am having with depthai and the OAK-D S2 Camera under Windows (but not under Linux)

### Requirements

Python 3.10 and pipenv (https://pipenv.pypa.io/en/latest/). Pipenv means we will always get the same dependencies and sub dependencies installed.

### Instructions

These instructions should work under both Linux and Windows.

Check out the repo and update the submodules.

Create a virtualenv

```
virtualenv venv
venv\Scripts\activate
```

Install depthai-python in the virtualenv
```
cd depthai-python
python -m pip install . -v
```

This will need to compile a lot of C++ code so will take awhile.

Install the other requirements
```
python -m pip install opencv-python numpy
```

Start the program up

```
python main.py 169.254.1.222
```
Assuming the camera is on the default ip address.

This will display the RGB image from the camera in a popup window in a continuous loop. Press 'q' while the popup window has the focus to shutdown in a controlled manner.

Under Linux this works flawlessly but under Windows I get the dreaded 'missing ping error message'.
