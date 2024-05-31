# Perceptual Qualities Python Toolkit

Toolkit for preparing and conducting experiments that asses
perceptual qualities of audio.

## Project for course WIMU 23Z

Project members:
- Bartłomiej Piktel
- Paweł Müller
- Grzegorz Rusinek

## Project structure

- docs - project documentation
- src - source files organised by modules
    - pq-toolkit - Python toolkit interface
    - pq-toolkit-ui - frontend for conducting experiments

## Usage

This project consists of test creation Python plugin and web application
testing platform.

### How to use Python plugin:
The project runs on [Python](https://www.python.org) 3.10+.

#### Installation

Firstly, you should obtain all project dependencies.
Consider using Python's [virtual environments](https://docs.python.org/3/tutorial/venv.html#virtual-environments-and-packages) to keep your installation nice and clean.

```bash
cd src/pq-toolkit
pip install -r requirements.txt
```

That's it! You're ready to go!

More detailed walkthrough can be found in project's docs directory.


### How to use testing web application:

1. Deployment:
   - Go to `src/pq-toolkit-ui`
   - Fill in required configuration in `.env.*` files according to your specification
   - Build docker image by running `make build-[flavor]`
   - Deploy docker image by running `make start-[flavor]`
2. Uploading experiments
   - Using Python script
   - Using admin panel available at `/admin`
3. Verifying configuration using admin panel (`/admin/[experiment-name]`)
4. Testing users `/[experiment-name]`
5. Getting results using Python script

More information available in `src/pq-toolkit-ui/README.md`.

## WIMU 24L notes

Known issues:
- Error handling
- Loading screen improvement (darkmode)

Potential improvements:
- more options for test configurations (new tests or more helper components)
- automatic mkdocs deployment
- dashboard in admin panel allowing to overview results
- implementation of sample playback functionality in the experiment configurator
