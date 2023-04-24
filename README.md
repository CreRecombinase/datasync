# Datasync, an Rclone Love Letter
Rclone is great, but remembering relevant paths in a scaled collaboration is _hard_. Use datasync to put your directories and bucket paths in a yaml format so you don't forget it! On top of that, having a command wrapper means you can easily drop this into any ci/cd process you have, or just run in it's own shell you continue on with your day.

## Usage
You can specify any `action` and datasync will perform that action on **all** entries in that action heading. Alternatively, you can specify `action entry` and datasync will only run that action on that entry.

Examples:  
*Perform a pull of every pull entry*
```
datasync pull
```
*Perform a pull of only the `foo` entry*
```
datasync pull foo
```

## Actions and intended workflow
**Pull** is a great way to sync down remote data locally. Think of it as *input* data.  
**Sync** performs bi-directonal non-destructive copying. Great for collaboration between locations/people.  
**Push** is intended to push data from your local to remote, ideal for *output* data.