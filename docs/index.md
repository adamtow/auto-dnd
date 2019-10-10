# Auto DND
Turn on Do Not Disturb mode on your iOS device based on calendar events that have a customizable string of your choice in the Title or Notes field. When used with Autocuts, Auto DND automatically does this for you throughout the day as you use your iOS device!

## Download
Get the latest version of Auto DND from RoutineHub:

- [**Auto DND on RoutineHub &raquo;**](https://routinehub.co/shortcut/3644)

## Getting Started
Here is a quick start guide to seeing how Auto DND works if you're running it for the first time:

1. Open Calendar.
2. Create a new event with the string "DND" in either the title or notes field.
3. Make sure the event is happening right now. For instance, if it's 12:35 pm, schedule the event to go from 12:00 pm to 1:00 pm.
4. Tap Done to save the new event to your calendar.
5. Launch Auto DND from the Shortcuts Home screen or the widget view.
6. By default, Auto DND will look for calendar events between 7:00 am and 10:00 pm. If the current time is outside of that range, tap Schedule and adjust the start and end times as necessary.
7. Ensure that Do Not Disturb is currently disabled.
8. Tap Check Now.

You'll see Do Not Disturb turn on based on an event in your calendar! Cool, eh? 

![Auto DND manually enabling Do Not Disturb based on calendar entry](https://adamtow.github.io/auto-dnd/images/auto-dnd-calendar.png)

Now, let's get it working automatically in the background.

### Autocuts
[Autocuts](https://adamtow.github.io/autocuts) works with the personal automations feature of Shortcuts in iOS 13 to run your shortcuts automatically in the background while you use your device throughout the day. Autocuts enables automatic running of shortcuts for triggers that previously required the user to tap a button in a notification banner.

To get Auto DND to run in Autocuts, do the following once you have installed the [Autocuts Admin](https://adamtow.github.io/autocuts) and [Autocuts Admin](https://adamtow.github.io/autocuts-admin) shortcuts and configure Autocuts to run as part of an Open App personal automation with your most frequently used apps.

1. Open the Autocuts Admin from the Shortcuts Home screen.
2. Tap New Autocut.
3. Select Auto DND.
4. Tap No Input.
5. Tap Immediately.
6. Enter -1 for the expiration time. This ensures Auto DND is called every time Autocuts runs.
7. Tap This Device ({{your device name}}) or Any Device if you want to run it on your other iOS devices attached to the same Apple ID.
8. Tap Run in Background.
9. Choose iCloud ({{your device name}}) if you chose This Device in Step 7. Otherwise, choose iCloud Drive (Shared) if you chose Any Device.

![Auto DND Autocut in Autocuts Admin](https://adamtow.github.io/auto-dnd/images/auto-dnd-autocuts.png)

The Autocut will have been created and will run any time the Autocuts personal automation is triggered by opening one of your selected apps.

Next, re-do the steps in the previous Getting Started section and create a calendar event with the string "DND" in either the title or notes field. Open one of the apps that will trigger Autocuts and you'll see Do Not Disturb turned on automatically!

![Auto DND in Action](https://adamtow.github.io/auto-dnd/images/auto-dnd-in-action.png)

#### But Wait, There's More!
Auto DND is but one shortcut that takes advantage of Autocuts. Check out [Location Triggers](https://adamtow.github.io/location-triggers) for running shortcuts automatically when you arrive or leave a location and [Auto Low Power Mode](https://adamtow.github.io/auto-low-power-mode) for turning on Low Power Mode when your battery percentage falls below a certain threshold.


## Interface
The following menu items appear when you launch Auto DND from the Shortcuts Home screen:

- [Automatically Set DND](#toggle)
- [Check Now](#run)
- [Require DND String](#require)
- [Do Not Disturb String](#string)
- [Schedule](#schedule)
- [Monitored Calendars](#calendars)
- [Use LimitKit](#limitkit)
- [Check Frequency](#frequency)
- [About](#about)
- [Help](#help)
- [Change Language](#language)
- [Check for Updates](#udpate)

<span id="toggle"></span>
### Automatically Set DND
The main switch for enabling and disabling Auto DND. When enabled, Auto DND will work automatically in the background provided you have created an Autocut in Autocuts to run it.

<span id="run"></span>
### Check Now
Evaluates your calendar entries and turns on Do Not Disturb mode if a matching event is found.

<span id="require"></span>
### Require DND String
When enabled, only events that have the Do Not Disturb String in the Title or Notes field will  cause Auto DND to automatically turn on Do Not Disturb mode. If disabled, any event will cause Do Not Disturb mode to be activated.

<span id="string"></span>
### Do Not Disturb String
A custom string to identify events where Do Not Disturb mode should be turned on. By default, it's DND.

<span id="schedule"></span>
### Schedule
Set the active times when Auto DND will work. If you have activated Scheduled Do Not Disturb in iOS, it's a good idea to set Auto DND's schedule to those hours outside of the system's schedule.

<span id="calendars"></span>
### Monitored Calendars
If left blank, all events in every calendar will be evaluated. Enter the names of your calendars, separated by new lines, to force Auto DND to evaluate events only in the selected calendars.

<span id="limitit"></span>
### Use LimitKit
LimitKit is an event logging system and rate limiting tool for shortcuts. Auto DND can optionally use LimitKit to adjust how frequently Auto DND evaluates your calendar.

<span id="frequency"></span>
### Check Frequency
When enabled, Auto DND will run every minute whenever it is invoked by Autocuts. So, if you run Autocuts manually or automatically several times in a minute, Auto DND will only run once. Every other time it's called, it will exit gracefully and quickly.

If you set the Check Frequency to 5, Auto DND will evaluate your calendar every five minutes. 

### About
Displays the about screen, with contains the current version and build number.

### Help
Displays the documentation that you are reading now.

### Change Language
Today, Auto DND is localized for the English language, but it's ready to be localized in any supported language by iOS. Please visit [Auto DND's GitHub page](https://github.com/adamtow/auto-dnd/tree/master/localization) and submit a pull request with a new localization file.

### Check for Updates
Checks to see if there is an update to Auto DND on RoutineHub.co. If an update is available, you will have the opportunity to download and install it onto your iOS device.

**NOTE**: *If you have enabled LimitKit, Auto DND will automatically check for an update once a week.* 
