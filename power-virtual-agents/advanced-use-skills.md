---
title: "Use Azure Bot Framework Skills in Power Virtual Agents"
description: "Extend your bot and author complex bot dialogs using pro-code tools to build Azure Bot Framework Skills that enable the bot to book an appointment, send a confirmation email, manage tasks, and more."
keywords: "authoring, extensibility, integration, extend bot, bot framework, skills, custom capabilities"
ms.date: 12/2/2019
ms.service:
  - dynamics-365-ai
ms.topic: article
author: iaanw
ms.author: iawilt
manager: shellyha
ms.custom: "azure, advanced-authoring"
ms.collection: virtual-agent
---


# Use Azure Bot Framework Skills in Power Virtual Agents

[This topic is pre-release documentation and is subject to change.]

Power Virtual Agents enables you to extend your bot using Azure Bot Framework Skills. If you have already built and deployed bots in your organization (using Bot Framework pro-code tools) for specific scenarios, you can convert bots to a Skill and embed the Skill within a Power Virtual Agents bot.

## Add a Skill to bot conversations
First, [create a Power Virtual Agents bot](authoring-first-bot.md) and [create and deploy the Skill using pro-code tools](https://go.microsoft.com/fwlink/?linkid=2110533) into your organization.

Next, [register a Skill in Power Virtual Agent](configuration-add-skills.md).

**Add a Skill into a conversation:**

1. Go to the [**Topics page**](authoring-create-edit-topics.md) for the bot you want to edit.

1. Open the authoring canvas for the topic you want to call a Skill action from.

1. Select the plus (**+**) icon underneath an existing node to add a new node. 

    ![Screenshot of adding a node](media/handoff-add-node.png)

1. In the node selection window, select **Call an action**, and then select the Skill you want to add. 

1. If your Skill has inputs, assign variables to those inputs. Also, if your Skill emits outputs to variables, you can use those variables in any nodes that follow. 

    >[!NOTE]
    >Skills can accept simple data types (integer, boolean, string) and complex data types (as JSON strings). 
    >If you need to extract variables from complex data types, you must [use Power Automate](advanced-flow.md) to further parse and break down complex JSON strings into key value pairs for use in your bot.

1. Select **Save** to persist your changes to the topic.

1. You should [test your bot](authoring-test-bot.md) to make sure it's using the Skill properly.


