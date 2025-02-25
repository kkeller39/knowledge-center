---
pagename: User guide
categoryName: Agent & manager workspace
subCategoryName: Agent tools for messaging
indicator: messaging
subtitle: 'Get acquainted with the agent workspace '
level3: ''
permalink: messaging-managers-user-guide.html
isTutorial: false
date: 2019-01-21 09:24:58 +0000
isNew: false
layout: newAgentWorkspace
---


## Configuration

To enable the manager workspace on your LiveEngage account, please contact your LivePerson account team. Once the feature is on, a new permission will be added to the agent manager profile called "View agent manager workspace". The permission is currently **“Off”** by default.

![](img/newworkspacepermissions.png)

### New agent workspace

Here you can also control the permissions for the new agent workspace. The permission is currently **“Off”** by default.

## Filters

Users will only be exposed to data related to the groups they manage. For example, an agent manager of the group "Sales" will only be able to view data and metrics which are driven from:

* Conversations which are currently waiting in queue in any of the skills assigned to the agents of group "Sales".
* Conversations which are currently assigned to agents of group "Sales".

The above assumes that no filters are enabled and thus represents the default view of the manager workspace.

The following filters can be applied to the sections listed above:

1. **Time filter** - by default, the workspace will show data from the last hour. Users will be able to change the time range to view data from the past X hours. The maximum supported time range is 24 hours.

![](img/timefilter.png)

{:start='2'}
2. **Group filter** - managers will be able to filter the data by a single group or a number of groups. The list will only contain groups and sub-groups the agent manager is managing, regardless of what this filter is set to.

![](img/groupfilter.png)

## Widgets

### In queue widget

The "in queue" widget presents the number of conversations currently waiting for agent assignment. The number will only include conversations associated with skills which are assigned to agents in groups the agent manager can view.

* The widget will not be impacted by the time filter or group filter available at the right top corner of the workspace.
* The widget is filterable by skill.
* A breakdown of "in-queue" conversations by skill is shown.
* Conversations assigned to the "UNASSIGNED" skill will also be included in the in queue conversations value.

![](img/new-manager-workspace-use-case-1.png){:class="newagent"}

### Metrics widget

The metrics widget provides a high level "health check" of your group’s real-time performance. The following metrics available:

* **ASSIGNED** - The number of open conversations currently assigned to logged in agents**. **Note**: This metric is not affected by the time filter.
* **LOAD** - The total weight of assigned conversations as a percentage of the maximum concurrent conversations of all agents. **Note**: This metric is not affected by the time filter.
* **CLOSED** - Number of conversations closed within the selected timeframe by the agent, the system or the consumer.
* **CSAT** - The percentage of questions which were answered with 4 or 5 (top two boxes) out of the total responses submitted by consumers to a CSAT question within the selected timeframe.

![](img/new-agent-workspace-1.png){:class="newagent"}

### Agents widget

The agent widget shows all agents under the manager which are currently logged into LiveEngage. Each agent card will show the following information:

* **AGENT STATUS** - The status of the agent: online, back soon or away. The away reason will be shown as well, if it exists. **Note**: This metric is not affected by the time filter.
* **ASSIGNED** - The number of open conversations being handled by the agent. **Note**: This metric is not affected by the time filter.
* **CLOSED** -  The number of conversations which were closed within the selected timeframe either by the agent, system or consumer while the agent was the assignee.
* **STATE DURATION** - Time since the agent last changed their state. **Note**: This metric is not affected by the time filter.
* **LOAD** - Total weight of the assigned conversations divided by the agent’s configured maximum number of high-intensity conversations. **Note**: This metric is not affected by the time filter.
* **CSAT** - The percentage of questions which were answered with 4 or 5 (top two boxes) out of the total responses submitted by consumers to a CSAT question within the selected timeframe. Attributed to the last assigned agent of the conversation.

![](img/new-agent-workspace-2.png){:class="newagent"}

### Conversations widget

#### Population

The conversation widget enables the manager to drill down to the conversation level. The conversation list will include:

* All open conversations.
* Conversations which were closed within the selected time frame (1 hour by default, up to 24 hours).

#### Columns

The list will include following columns:

* **STATUS**- The status of the conversation. The conversation can be in one of the following statuses:
  * _In queue_ - conversation is waiting in queue to be assigned to an agent.
  * _Assigned_ - conversation is currently being handled by an agent.
  * _Closed_ - conversation is closed (by agent, system or consumer). Conversations which are currently in post-survey status are considered closed.
* **AGENT NAME** - The name of the agent currently assigned to the conversation.
* **SKILL** - The current skill of the conversation.
* **CONSUMER** - The name of the consumer. Clicking on the consumer name will open the conversation window .
* **RESPONSE TIME** - The duration of time remaining until a response is required.
* **MCS** - Meaningful Connection Score.
* **CSAT** - Customer satisfaction rated from 1 to 5, as submitted by the customer within the survey.
* **NPS** - Customer Net Promoter Score rate from 0 to 10, as submitted by the customer within the survey.

#### Navigating to the conversation

Clicking on the consumer name will open the conversation window. Only open conversations ("in-queue", “assigned” statuses) will be clickable. Once in the conversation view, you will see the option to join the conversation. If you choose to join the conversation it will be moved to your My Connections list.

{: .notice}
**Please note:** If the new agent workspace is not toggled on, when you select a conversation you will be redirected to the All Connections list in the old UI.

![](img/conversationswidget.png)

#### Filtering the list

In addition to the group and time filters at the top of the dashboard, the list can be filtered by the agent name and/or the conversation status (in-queue, assigned, closed).

Filtering by agent name will retrieve:

* The conversations the agent is currently assigned to.
* Closed conversations that the agent was the last to handle.

#### Sorting the list

The list is sortable by "Response time". The list will be sorted by default by “Response time”, so that conversations which are waiting the longest will be placed at the top of the list.

## Limitations

* The workspace presents messaging agents’ data and messaging metrics. Chat agents and performance are not part of the workspace.
* The agents widget is limited to show a maximum number of 500 agents.
* The minimal supported screen resolution is 1024x768.
* The data presented are refreshed at a maximum of every 40 seconds from the time of login and may vary slightly from what is presented in LiveEngage due to refresh-rate differences.

## Known issues (bugs)

Following issues are scheduled to be resolved within the next release:

### General

* The Internet Explorer 11.0 (or earlier versions) browser is not supported.
* The dashboard is available only in the English language.

### Agents widget

* The widget flickers when it refreshes.

### Conversation widget

* Currently limited to show a maximum number of 50 conversations.
* When using both agent filter and group filter, conversations from all groups and agents are retrieved.
* In case the conversation was sent back to queue or transferred to a different agent or skill, the agent name column shows the name of transferring agent instead of showing "N/A".
* When filtering by agent name, conversations which the agent is currently not assigned to but was the assignee at some point, are retrieved.
