# iLEAPP

iOS Logs, Events, And Preferences Parser  
Details in blog post here: <https://abrignoni.blogspot.com/2019/12/ileapp-ios-logs-events-and-properties.html>

Supports iOS 11, 12 & 13.
Select parsing directly from a compressed .tar/.zip file or a decompressed directory.

## Features

Parses:  
⚙️ Mobile Installation Logs  
⚙️ iOS 12 & 13 Notifications  
⚙️ Build Info (iOS version, etc.)  
⚙️ Wireless cellular service info (IMEI, number, etc.)  
⚙️ Screen icons list by screen and in grid order.  
⚙️ ApplicationState.db support for app bundle ID to data container GUID correlation.  
⚙️ User and computer names that the iOS device connected to. Function updated by Jack Farley (@JackFarley248, <http://farleyforensics.com/>).  
⚙️ KnowldgeC + Powerlog artifacts.
And many, many more...

## Installation

Pre-requisites:
This project requires you to have Python > 3.7.4 installed on your system.

To install dependencies, run:

```bash
pip install -r requirements.txt
```

To install dependencies offline Troy Schnack has a neat process here:
<https://twitter.com/TroySchnack/status/1266085323651444736?s=19>

To run on **Linux**, you will also need to install `tkinter` separately like so:

```bash
sudo apt-get install python3-tk
```

## Compile to executable

To compile to an executable so you can run this on a system without python installed.

To create ileapp.exe, run:

```bash
pyinstaller --onefile ileapp.spec
```

To create ileappGUI.exe, run:

```bash
pyinstaller --onefile --noconsole ileappGUI.spec
```

## Usage

### CLI

```bash
python ileapp.py -t <zip | tar | fs> -i <path_to_extraction> -o <path_for_report_output>
```

### GUI

```bash
python ileappGUI.py
```

### Help

```bash
python ileapp.py --help
```

The GUI will open in another window.
