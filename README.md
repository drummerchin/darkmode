# Dark Mode

Since macOS 10.14 Mojave, dark mode can be set by "System Perferences" -> "..." -> "...".

In apple script, we can set appearance to dark mode as below:

```
tell application "System Events"
    tell appearance preferences
        set dark mode to not dark mode
    end tell
end tell
```

Or written in one line like this:

```
tell application "System Events" to tell appearance preferences to set dark mode to not dark mode
```

I highly recommend that you use alias in your .bash_profile :

```bash
echo -e "alias darkmode="\""osascript -e 'tell application "\""\\"\"""\""System Events"\""\\"\"""\"" to tell appearance preferences to set dark mode to not dark mode'"\""" >> ~/.bash_profile
```

to swith darkmode, run:

```
darkmode
```

if you're already in dark mode, run it again, you'll go back from dark mode.

Note: this script requires privilleges, you can set it in your System Preferences.
