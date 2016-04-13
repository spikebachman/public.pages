## 4/7/16
# SP Slack/Workfront Automation Commands Cheat Sheet

### Hint: To see a link to this cheatsheet in Slack, type /wf help
---

If you would like an easy way to use Slack to handle a project's team messaging, notes, attachments, etc., then start by creating a new Slack project channel or go to an existing project channel. (If you make a new project channel, use the associated referenceId in the channel title)

**Example: 112233-proj_title**

Then invite @wf to the channel

**Example: /invite @wf**

In addition, if @wf doesn’t know you, she will nag you when you post to associate yourself with a Workfront account.

**Example: /wf set user sbachman@samaritan.org** (If prompted, associates your slack account with the approriate Workfront Account.


### Commands
---

**/wf set default project {{referenceId}}** - Sets a default project that /wf work create/complete/stop will fall under.

**/wf work create {{description}}** - Creates a new task plus starts the timer for it in your default project and adds it to the current iteration.

**/wf working {{referenceId}}** - Moves the referenced task into the current iteration, into the 'In Progress' lane and starts a timer for it.

**/wf complete** - Moves the working task to completed and log the time.

**/wf stop** - stops the timer on the working task and moves it back to new and logs the time.

**/wf tasks** - Shows you a list of your tasks.

**/wf projects** - List of projects you are on. [Not yet implemented]

**/wf note {{note text}}** - Makes a note on your working task.

**/wf status** - Shows you your timesheet, current working task & iteration/board.

**/wf boards** - Links to current iteration.


### Markup
---

    !This is a comment I don't want to log into Workfront.
(A '!' at the beginning of a comment will not logged it into Workfront)