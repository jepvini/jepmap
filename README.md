# Jepmap

jepmap is a simple bash script to set and monitor the power settings of your cpu\
*written instead of studying by jep*

### Why?
I made this script for my Lenovo thinkpad E14 gen 5, with an intel 1335u (model number LENOVO 21JKCTO1WW)
The laptop has a strange thermal limit at 80C which cuts the continuous power at roughly 25 watts
I'm still investigating this issue...

### How?
The idea is to write an *alias script* that makes easier to set and read values without the need to remember long and complex commands

The core of the project is the [ setPL ](https://github.com/horshack-dpreview/setPL) by horshack-dpreview

### Dependencies
diclamer: I'm using `NixOs` (and you should yse it too 'couse it's awesome), the pkgs' name from Nix
- setPL
- turbostat

turbostat needs the `msr` kernel module, if it is not loaded just run
`# modprobe msr`

### Usage

sudo is mandatory!!!

jepmap        Get PL1 and PL2 values
jepmap get    Get powerstat summary and monitor some cpu info (mainly power usage and temp)
jepset N      Set PL1 and PL2 to N using setPL by horshack-dpreview
jepset hi     Set PLs to HIGH set in the script
jepset mid    Set PLs to MID set in the script
jepset lo     Set PLs to LOW set in the script

any other argument will print the help prompt
