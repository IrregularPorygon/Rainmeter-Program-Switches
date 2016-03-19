# Rainmeter-Program-Switches
Automatically produces rainmeter skins to run programs on and off

Note: This is windows only

## Setup

First, download a zip of the repository, and extract it into your Rainmeter directory, for example: C:\Users\<User Name>\Documents\Rainmeter

(You can extract it anywhere you want, if you would rather put it in another directory. The only caveat is that you'll have to manually copy the skins folder once the build is complete)

Next, open up info.json. It should look something like this:

```
{
    "Notepad" : {
        "path": "C:\\Windows\\System32\\notepad.exe"
    },
    "Skype" : {
        "path": "C:\\Program Files (x86)\\Skype\\Phone\\Skype.exe"
    },
    "Dropbox" : {
        "path": "C:\\Program Files (x86)\\Dropbox\\Client\\Dropbox.exe"
    }
}
```

This is how you tell the build which applications you want it to create skins for. The path is the location to the executable, the title is the name the skin with have.

For every application that you list, you need a correponding image file (.png) in the Images folder. Make sure that it has the same name as the title in the info.json file, for exmaple, with the above info.json, you'll need to have

* Images/Notepad.png
* Images/Skype.png
* Images/Dropbox.png

## Running the build

Once all of that's done, open up command prompt (run -> cmd) and navigate to the directory that you extraced to. (i.e. cd C:\path\to\extracted\folder)

Then, run "gradlew build"

The build process will then go through each entry that was listed, and create folders under Skins/ProgramSwitches. After the build finishes, you should be able to refresh all in Rainmeter and have all the newly generated skins!