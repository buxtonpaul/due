# due
A [todo.txt](http://todotxt.com/) plugin to display your due and overdue tasks using Python 3.

In order to use this plugin, tasks must be added with due dates in the format:
```
due:YYYY-MM-DD
```
Note that the keyword 'due' can be modified by setting the TODO_TXT_DUE_KEY environment variable.

# Installation

In order to install actions in sub-directories of the add-on directory, please use todo.txt [version 2.10](https://github.com/ginatrapani/todo.txt-cli/releases/tag/v2.10). Following [Installing Add-ons](https://github.com/ginatrapani/todo.txt-cli/wiki/Creating-and-Installing-Add-ons), first `cd`
into your `.todo.actions.d` directory. The default location is within `$HOME`:
```
cd ~/.todo.actions.d
```

Clone this repository:
```
git clone https://github.com/rebeccamorgan/due.git
```

Now make the `due` shell script executable:
```
chmod +x due
```

# Usage
Default behaviour displays tasks that are overdue, due today or due tomorrow:
```
todo.sh due
```

An optional argument of an integer n will also print the tasks due in the next n days (not including today). For example, to also see tasks due in the next week:
```
todo.sh due 7
```
Passing a value of 0 will show only tasks overdue or due today, omitting tasks due tomorrow.
