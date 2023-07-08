# clrk

Clrk (clerk) aims to establish itself as a time management assistant that can be setup to suit a variety of approaches to time management.

## Project Overview

In aiming to be modular and flexible so as to be able to be used to fit the specific needs of any given user, the project will be spread out across a number of packages:

### @clrk/core
This package contains the core functionality that any implementation of the larger *clrk* project will require. This package is essentially a bare bones CLI utility that enables the configuration of the users details and from this utility you are able to select and install the various other packages that you need.

### @clrk/task
This package enables a simple todo list:
- As a user, I want to...
  - create a new task with the following properties
    - name, description (optional), due date (optional, date-time), estimated time (optional, in minutes), completed (default false)
  - update an existing task (any property)
  - view the date created and updated for a given task (read only)
  - delete a task
  - be prevented from creating two tasks with the same name incomplete tasks nly ordered by due date then date created
  - view tasks in a list view
  - filter and order tasks by completed, due date, date created, and date updated
  - have the task view default to be a list of incomplete tasks ordered by due date then date created
  - search for tasks by name

### @clrk/project
This package contains features for projects, which are essentially task containers that enable a step-like flow for the contained tasks, and optional milestones, among other things.

### @clrk/habit
This package contains features that enable the creation of habits, records similar to tasks except containing a recurrence pattern / schedule rather than a due date, and a history of completion (by way of marking a habit as done for a given instance) rather than a single boolean.

### @clrk/inbox
This package adds a list which contain "notices (find a better name)", simple records that have a name and a description, the idea being these items are pending a process of going through and either converting them to tasks, notes on a record, etc, or deleting them, this "process" being a feature of this package as well, where you are able to initiate a processing session and are guided through each item in the inbox and for each one, are able to select how to process it, until the inbox is cleared.

### @clrk/notes
This package adds notes as a property of records, enabling a note history and the ability to set up default note creating for changes to the record (a simple change log feature).

### @clrk/calendar
This package contains features related to the calendar, specifically a calendar view which enables a view with a set of days (defaults to current week, also enables 3 day view, month view, and day view) with scheduled tasks (tasks with a due date) 

### @clrk/core
This package contains the core functionality that any implementation of the larger *clrk* project will require.

