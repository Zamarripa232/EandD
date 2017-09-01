# Excel and Dragons Writing Tracker

You can't see where you're going without knowing where you are.

This spreadsheet can be used to keep track of writing sprints, daily writing goals, etc. and track the corresponding time.

Included are formulas and conditional formatting for a "minion" health bar, "boss" health, and a few achievements. 

* The minion health bar represents a target goal writing speed that is calculated by multiplying your first tracked speed by 1.5. This can be modified in the formula or updated as you need. It only tracks against the most recent writing sprint to show how well you fought.

* Boss health represents progress along major projects. For example, a 70,000 word novel. 

# Usage
I don't feel this needs explanation, but whatevs.

1. Click an empty Start cell in column C
2. Press Ctrl + Shift + ;   (or enter the time you started in the following format h:mm:ss AM/PM)
3. Keep writing.
4. When you finish a sprint, update the time in column D
5. Place your word count in column A
6. The rest of the sheet should autopopulate.


# Clearing out existing data
Only delete data from the yellow columns, all others are formulas you shouldn't touch if you don't know what you're doing.

Or touch them. I'm not your boss.

# Seconds for Time Input
If you would like a more prescise time input at Ctrl + Shift + ;, then you'll need to add the following to your macros. I personally am not in favor of distributing Excel files with embedded macros so I leave it here since it's small enough. Afterwards, just run the setKey macro and you're ctrl+shift+; will add seconds now.

Sub setKey()
    Application.OnKey "+^:", "EnterTime"
    End Sub
Sub resetKey()
    Application.OnKey "+^:"
    End Sub
Sub EnterTime()
    With ActiveCell
    .Value = Time()
    .NumberFormat = "hh:mm:ss"
        End With
    End Sub



# Adding more chievos/features/whatnot
Go right ahead, these are mostly examples I thought would be fun. I can't imagine I'm going to iterate this into a fully featured AD&D Temple of Elemental Evil campaign though.

Well, now that I mention it, that does sound kinda cool.
