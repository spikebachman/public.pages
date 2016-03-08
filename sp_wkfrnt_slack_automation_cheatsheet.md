## 3/6/16
# SP Slack/Workfront Automation Commands Cheat Sheet
---

To begin, create a new Slack project or task channel or go to an existing channel. (If you make a new project/task channel, let's try using the associated id in the channel title)

**Example: 112233projtitle

Then invite @wf to the channel

**Example: /invite @wf**

Then you’ll want to associate it with the WF project/task' id you'll be referencing:

**Example: @wf set project 112233 –or– @wf set task 445566**

In addition, if @wf doesn’t know you, she will nag you when you post to associate yourself with a Workfront account

**Example: @wf set user sbachman@samaritan.org**

Note: There are two task types:
1. Your **active task** which follows you around in Slack, which is running a timer for you
2. Your **channel task** which reside inside lack project and task channels and which record your notes into WF

### Commands
---

**@wf: status** (Shows the current channel configuration)
    
**@wf: set user email@domain.com** (If prompted, associates your slack account with the approriate Workfront Account. *Updates aren’t currently working 3/6/16*)
    
**@wf: set project 112233** (Associates comments with the supplied reference Id for the Workfront Project. Use when you are not working inside a particular project's slack channel)

**@wf: set task 445566** (Associates comments with the supplied Workfront task id)

**@wf: leave** (Stop Workfront logging from the Slack channel)

**@wf: comeback** (Resume Workfront to logging from the Slack channel)

**@wf: link** (Returns the link for the channel and also gives a link for your current working task if there is one)

**@wf: list** (Returns a list of projects and reference Ids for the current sprint)

**@wf: tasks** (Returns a list of tasks and reference Ids that are assigned to you and not yet complete)

**@wf: working 778899** or **@wf: work 778899** (Sets the task identified by reference id as the active task and starts a timer)
    
**@wf stopped 778899** or **@wf stop 778899** (Moves the active task back into new status and logs the time spent)
    
**@wf complete 778899** or **@wf done 778899** (Moves the active task into completed status and logs time spent)

### Markup
---

    !This is a comment I don't want to log into Workfront.
(A '!' at the beginning of a comment will not logged it into Workfront)

    *This is a comment that will log to my working task, instead of the channel task/project.
(An '*' at the beginning of a comment will log it to your working task)

*Note: If you are in a direct message @wf, it is not necessary to include the @wf at the start of the line.*