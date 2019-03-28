## tw-agenda-hook

In short; 
- sched:date means do/complete a task on that date, but it has no deadline
- due:date when tasks are actually due (have a hard deadline) 
- until:date for those tasks that can't be done after that date (like "go to event")
- wait:date for those tasks you don't want to see till then

These 4 pieces of information are automatically merged into a new property: effective date.

### Todo 1. ###

Find out whether it automatically exports to agenda (in order of sorted effective date) (using the estimated duration to actually schedule the work , otherwise implement it and compare it to the urgency scheduling method. (Highest urgency first, use estimated duration of tasks to add them to your calendar. {define the constraints of your calendar with davdroid, and recurring tasks (eat clean laundry +sleep etc) that should be automatically exported to your calendar [AND/OR  the other way round!].})

### Todo 2. ### 

Auto "sms" if scheduling conflict is detected/arises

### Todo 3. ### 

Add algorithm 1ng to improve estimated duration forecasting.


status: Working well, still in testing

caveat: Perpetual Proof of Concept, until a "real programmer" can apply some real expertise, but it worksforme.

see also: needs.txt help file for more detailed how-it-works/ install/ config/ usage/ contrib suggestions.

### Features

- hook-script automatically generates edate for all new and modified tasks
- check_edate script provided, to batch-process tasks when getting started

new reports;
- agenda
- agd (today)
- agt (tomorrow)
- agw (this week)
- agnw (next week)
- agm (this month)
- agnm (next month)
- agx (before now)
- edate (diagnostic)

These reports can be used in combination with any other task filters, so that _'task pro:foo agw'_ (for example) will show all foo project tasks that are "on your agenda" for this week. 

(edate can also be used in your own reports)

#### Planned features

### Advantages

Without this extension, tasks can only be sorted by due OR sched OR until OR wait, and the user has to choose which ONE of these dates to use as a primary sort. This can force the user to apply hard-due-dates (for example) where a sched:date might be more accurate. Similarly, with this extension, users can assign just a wait:date, or an until:date, or any combination, and those tasks will be shown in chronological sequence, along with tasks that might have only a due:date or sched:date.

SCREENSHOT

### Benefits

Taskwarrior users with this extension can assign the whichever type of date (sched, due, until, wait) that makes sense for the specific task.

- sched:date when you decide you want to do a task, but with no external deadline
- due:date when tasks are actually due (have a hard deadline) 
- until:date for those tasks that can't be done after that date (like "go to event")
- wait:date for those tasks you don't want to see till then

in whatever combination of dates you choose, those tasks will be sorted together according to "effective date".

### Bugs/ Feature requests/ Pull requests

fork/ file issues/ comment at https://github.com/linuxcaffe/tw-agenda-hook

### Credits

- concept and config files cobbled together by djp
- hook-script written by bqf 
