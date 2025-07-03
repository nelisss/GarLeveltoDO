# GarLeveltoDO

This project allows you to convert Garmin Connect and Strength Level activities to a format that can be imported into a Day One journal.

## Table of Contents

- [Installation](#installation)
- [Usage](#usage)
- [Contributing](#contributing)
- [License](#license)

## Installation

Currently, this project is probably quite unusable. I have made the scripts to suit my needs, which means that they aren't likely to work for your needs. Garmin also has the annoying habit of changing column names every so often. Will be improved!

Required:

- Python>=3.9
- Jupyter notebook (or vscode, google colab)

### Python virtual environment (venv) installation

Steps (Windows):

1. Open a terminal/command prompt and change directory into a folder where you want to create a venv

        cd path\to\folder

2. Create a venv and give it a name

        python -m venv venv_name

3. Activate the venv

        venv_name\Scripts\activate

4. Install required packages into the venv by using requirements.txt (change path to directory where requirements.txt is located)

        pip install -r \path\to\requirements.txt

Steps (Linux/MacOS):

1. Open a terminal and change directory into a folder where you want to create a venv

        cd path/to/folder

2. Create a venv and give it a name

        python -m venv venv_name

3. Activate the venv

        source venv_name/bin/activate

4. Install required packages into the venv by using requirements.txt (change path to directory where requirements.txt is located)

        pip install -r /path/to/requirements.txt

## Usage

Run the scripts from top to bottom, input the files when prompted. To download the csv files:

- Garmin Connect csv: from https://connect.garmin.com/modern/activities, scroll down as far as you want and press Export CSV.
- Strength Level csv: from https://my.strengthlevel.com/username/workouts (replace username with your username), scroll down to the bottom of the page and press Export CSV.

## Roadmap

- [ ] Add venv installation (requirements.txt)
- [ ] Unify notebooks
- [ ] Improve generalizability
- [ ] Create .exe installer
- [ ] ...

## License

This project is licensed under the GNU General Public License 3.0 - see the [LICENSE](LICENSE) file for details.

