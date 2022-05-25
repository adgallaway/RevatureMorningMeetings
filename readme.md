readme.md

# Revature.Morning.Meetings
    Opens Edge browser
    Opens Outlook website
        logs into Revature email
            uses Orchestrator credentials
    Opens Rev Pro in a new tab
        logs into Rev Pro
            uses Orchestrator credentials
        navigates to curriculum calendar
        check-marks the 'CHECK-IN' box
            Try Check 'Check-In'
            Catch Exception
                logs exception at Warn level
            Catch ElementOperationException
                logs exception at Warn level
                invokes workflow to use Click
                    Try Click
                    Catch ElementOperationException
                        logs exception at Warn level
                    Catch Exception
                        logs exception at Warn level
    Uses Now.DayOfWeek.ToString to get current day of week
        assigns meeting name to string variable based on the day of the week
    Invokes ZoomMeetings Process
        passes meeting name in argument
    Invokes TimeSheetAutomation Process when day of the week is Friday
