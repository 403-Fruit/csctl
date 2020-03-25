# csctl
Scripting CS:GO over telnet.

## Description
Execute cs:go commands from a file over telnet. This allows you to control execution timing and allows you to script usercmds (+left, +jump, etc.)  

Tested on Python 3.7.4 but not extensively.  

Big thanks to [@nibalizer](https://github.com/nibalizer) for [this project](https://github.com/nibalizer/csgo_remote_control), which was a huge help in figuring out how to interface with the client

## Setup
    git clone https://github.com/403-Fruit/csctl.git
    cd csctl
    pip3 install -r requirements.txt

## Usage
Add the following launch option to CS:GO  

    -netconport 2121  

Run the script  

    python3 csctl.py

Then in-game you can run  

    echo exectn <instruction_file>

Or bind to a key with  

	bind "<key>" "echo exectn <instruction_file>"

This will execute commands from *instruction_file*, or if the line is *delay x.x*, sleep for *x.x* seconds.  

## Notes
- Instruction files can be placed in CS:GO's config directory, or the same directory as csctl.py.  
- Example instruction files are included in the examples folder. (stutter_step.csctl, echo.csctl)
