# 2025 Microscopy & Microanalysis HyperSpy Workshop

Training material used during the 2025 HyperSpy Workshop at the Microscopy and Microanalysis meeting in Salt Lake City, UT
in the short course _X-10 EM Data Analysis with the HyperSpy Ecosystem_.

## Pre-course instructions

> [!CAUTION]
> TODO: make release and add button to download files

Prior to arriving at the short course, please do the following:

1. Install HyperSpy (see the [software installation](#software-installation) section)
1. Download the example notebooks by clicking the button below and extract the Zip file to a folder on your system

<!-- HTML !-->
<div style="margin-left: auto; margin-right: auto">
<a href="https://github.com/hyperspy/MM2025_HyperSpy_Workshop/archive/refs/heads/main.zip">
<button style="appearance: none;
  background-color: #2ea44f;
  border: 1px solid rgba(27, 31, 35, .15);
  border-radius: 6px;
  box-shadow: rgba(27, 31, 35, .1) 0 1px 0;
  box-sizing: border-box;
  color: #fff;
  cursor: pointer;
  display: inline-block;
  font-family: -apple-system,system-ui,'Segoe UI',Helvetica,Arial,sans-serif,'Apple Color Emoji','Segoe UI Emoji';
  font-size: 14px;
  font-weight: 600;
  line-height: 20px;
  padding: 6px 16px;
  position: relative;
  text-align: center;
  text-decoration: none;
  user-select: none;
  -webkit-user-select: none;
  touch-action: manipulation;
  vertical-align: middle;
  white-space: nowrap;" role="button">Download Course Files</button>
  </a>
  </div>


### Getting started

To run the demo notebooks in this tutorial, you will need to use the "Jupyter Lab" application, which will allow you to evaluate the Python code and follow along with the instructors.

Depending on how you installed HyperSpy, how you start Jupyter Lab will look different:

- If you used the HyperSpy bundle:
    - (on Windows): you will find the "HyperSpy-bundle prompt" in your Start Menu. Open this application, and change to the directory where you unzipped the files via the [`cd` command](https://www.geeksforgeeks.org/operating-systems/cd-cmd-command/). Once in the right directory, execute the `jupyter lab` command to start Jupyter
    - (on MacOS or Linux): from a terminal window, change to the directory where you unzipped the files, and execute the `jupyter` command from the `bin/` directory of the bundle installation. This will look something like: 
        - `cd /Users/username/Downloads/hyperspy_tutorial/`
        - `/Users/username/hyperspy-bundle/bin/jupyter lab`
- If you used the manual `conda` method:
    - Either open an "Anaconda Prompt" window, or activate the base `conda` environment in a regular terminal
    - Activate the conda environment you created for the tutorial with `conda activate hyperspy_MM2025`
    - Change to the directory where you unzipped the files
    - Start Jupyter by running `jupyter lab`

Assuming this was successful, you should see the Jupyter Lab application open in your default web browser. The application runs in the background, and you access it via a regular browser window. If you can see the tutorial files, you're good to go! If not, please come to the short course a little early, and the instructors will help you get your installation set up correctly.

## ✨ Try it in your browser ✨

While we recommend downloading this repository and running the code locally (since that will be how you use
HyperSpy on your own data), you can use the following link to interactively run these tutorial files
in your web browser during the course.

[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/hyperspy/MM2025_HyperSpy_Workshop/HEAD)

Otherwise, follow the instructions in the previous section to get started.

## Venue

Room 151 A, Salt Palace Convention Center, Salt Lake City, UT. 

## Agenda

The workshop will take place from 8:30 to 17:00 MDT on Sunday the July 27, 2025. The program will officially
start at 8:45, but the instructors will be present from 8:00 onwards to assist anyone with installation issues
before the course begins.

| Time         | Length | Activity                                                                   | Presenter            |
|--------------|--------|----------------------------------------------------------------------------|----------------------|
| 8:30-8:45    | 15m    | Welcome / installation help                                                |                      |
| 8:45-9:00    | 15m    | Introduction talk                                                          | Josh Taillon         |
| 9:00-10:15   | 1h15m  | 1. Getting started / HyperSpy Basics                                       | Josh Taillon         |
| 10:15-10:30  | 15m    | Coffee break                                                               |                      |
| 10:30-11:15  | 45m    | 2. Decomposition and BSS                                                   | Josh Taillon         |
| 11:15-12:00  | 45m    | 3. Curve fitting                                                           | Carter Francis       |
| 12:00-12:45  | 45m    | Lunch break                                                                |                      |
| 12:45-13:30  | 45m    | 4. EDX with [eXSpy](https://hyperspy.org/exspy/)                           | Carter Francis       |
| 13:30-14:15  | 45m    | 5. EELS with [eXSpy](https://hyperspy.org/exspy/)                          | Josh Taillon         |
| 14:15-14:30  | 15m    | Coffee break                                                               |                      |
| 14:30-15:15  | 45m    | 7. Lazy signals for Big Data                                               | Carter Francis       |
| 15:15-16:00  | 45m    | 8. 4D-STEM with [Pyxem](https://pyxem.readthedocs.io/en/stable/index.html) | Carter Francis       |
| 16:00-17:00  | 1h     | Extra time / Office hours / "Bring your own data"                          |                      |


During the final hour, the instructors will be available in a casual setting to answer specific questions about how HyperSpy could be used with your data. Please bring data from your research to play with during this time!

## Instructors

- Joshua Taillon ([DataSophos, LLC](https://datasophos.co))
- Carter Francis (Direct Electron)

## Helpers

- Nick Hagopian (UW Madison)
- Geri Topore (Imperial College London)

## Software installation

To use the Jupyter Notebooks in this repository, you need to install some software packages first. Installation instructions for beginners and advanced users can be found below.


### Simple installation instructions (best for Python beginners)

The easiest (and recommended) way to install the software required to run the Jupyter Notebooks in this repository is to [install the HyperSpy Bundle](https://hyperspy.org/hyperspy-bundle/install.html), which can be downloaded from [here](https://github.com/hyperspy/hyperspy-bundle/releases/latest).


### Advanced installation instructions (for advanced users)

If you prefer to customize your installation, we suggest installing a conda distribution (we suggest [MiniForge](https://github.com/conda-forge/miniforge)) and install all the required Python packages in a dedicated environment executing the following commands in a terminal (the conda prompt in Windows):


```bash
conda install nb_conda_kernels jupyterlab start_jupyter_cm ipympl -c conda-forge
conda create -n hyperspy_MM2025 python=3.11 hyperspy pyxem ipympl exspy lumispy ipykernel -c conda-forge
```

To use HyperSpy in JupyterLab, start Jupyter Lab and choose the `Python [conda env:hyperspy_MM2025]` kernel. Alternatively, start JupyterLab from the `hyperspy_MM2025` environment as follows:

```bash
conda activate hyperspy_MM2025
jupyter lab
```
