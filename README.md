# Sidecar-toggle-alfredworkflow

An alfred workflow to toggle Sidecar in Big Sur.

## Mechanism (latest)

The script is modified from [geofftaylor/connect-sidecar](https://github.com/geofftaylor/connect-sidecar/blob/main/Connect%20Sidecar%20-%20Big%20Sur.applescript). The change is replacing "Control Center" to "Control **Centre**" in the script, which should be possibly due to language and region setting in Mac. Without this change the script will report error, that "Control Center" cannot be found.

Suggested steps to checkout for this option in advanced:

1. Open "Script Editor"
2. Enter the code below and run it in the "Script Editor"
   ```
   tell application "System Events"
       tell its application process "ControlCenter"
           every menu bar item of menu bar 1
       end tell
   end tell
   ```
3. Check whether "Control Centre" or "Control Center" is shown in the "Result" pane.
