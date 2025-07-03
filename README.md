# GarLeveltoDO

This project allows you to convert Garmin Connect and Strength Level activities to a format that can be imported into a Day One journal.

## Table of Contents

- [Installation](#installation)
- [Usage](#usage)
- [Roadmap](#roadmap)
- [Issues](#issues)
- [License](#license)

## Installation

Currently, this project is probably quite unusable. I have made the scripts to suit my needs, which means that they aren't likely to work for your needs. Garmin also has the annoying habit of changing column names every so often. Will be improved!

Required:

- Python>=3.9
- Jupyter notebook (or vscode, google colab)

### Python virtual environment (venv) installation

To ensure that the code works on your system, I recommend creating a virtual environment with package versions as given in requirements.txt.

Steps (Windows):

1. Open a terminal/command prompt and change directory into a folder where you want to create a venv

        cd path\to\folder

2. Create a venv and give it a name

        python -m venv venv_name

3. Activate the venv

        venv_name\Scripts\activate

4. Install required packages into the venv by using requirements.txt (change path to directory where requirements.txt is located)

        pip install -r \path\to\requirements.txt

5. Use the venv as python interpreter when running the notebooks

Steps (Linux/MacOS):

1. Open a terminal and change directory into a folder where you want to create a venv

        cd path/to/folder

2. Create a venv and give it a name

        python -m venv venv_name

3. Activate the venv

        source venv_name/bin/activate

4. Install required packages into the venv by using requirements.txt (change path to directory where requirements.txt is located)

        pip install -r /path/to/requirements.txt

5. Use the venv as python interpreter when running the notebooks

## Usage

### Download the CSV files

- Garmin Connect CSV: from https://connect.garmin.com/modern/activities, scroll down as far as you want and press Export CSV.
        
  - Only the activities that are loaded on the web page will be exported into the CSV file. This can cause problems when you want to export a lot of activities. However, I don't know of any other way to batch export activities into a CSV file.

- Strength Level CSV: from https://my.strengthlevel.com/username/workouts (replace username with your username), scroll down to the bottom of the page and press Export CSV.

### Run the scripts

*GarLeveltoDO.ipynb:*
Takes Garmin and/or Strength Level CSVs as input and outputs a CSV that can be imported into a new Day One journal.

Run the script from top to bottom, choose Garmin, Strength Level, or both, input the CSV file(s) and select a start date when prompted. 

*GarminStats.ipynb:*
Takes Garmin CSV as input gives some stats and graphs.

Run the script from top to bottom, input the Garmin CSV when prompted. 

*SLStats.ipynb:*
Takes Strength Level CSV as input gives some stats and graphs.

Run the script from top to bottom, input the Strength Level CSV when prompted. 

### Import in Day One
To import the CSV into Day One, follow the instructions on the [Day One website](https://dayoneapp.com/guides/settings/importing-data-to-day-one/). Currently, CSV import is only supported on iOS. 

To import the ZIP file with JSON content into Day One, follow the instructions for your platform of choice on the [Day One website](https://dayoneapp.com/guides/settings/importing-data-to-day-one/). JSON import is supported on all platforms, I've tested on the Web App and iOS. Both work for me, but Web App import is quite slow.

### Notes
- The timezone of the system that runs the script is used. I'm unsure of what timezones are used for the output CSVs, so the output times might not correspond to actual times.

## Roadmap

- [x] Add venv installation (requirements.txt)
- [x] Unify notebooks
- [x] Add other output formats (JSON zip)
- [ ] Improve generalizability by adding supported Garmin activities
  - Currently supported Garmin activity types: Running, Hiking, Walking, Treadmill Running, Cycling, Mountain Biking, Open Water Swimming, Pool Swim.
  - Unsupported activities will only show some very generic info, and some might not work at all.
- [ ] Create .exe installer
- [ ] ...

## Issues
- Many
- ~~ZIP import on iOS is currently not working, gives an error (DOCore.DOImporterError error 1)~~

## License

This project is licensed under the GNU General Public License 3.0 - see the [LICENSE](LICENSE) file for details.

