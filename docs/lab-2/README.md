---
title: Refinining your watsonx assistant
description: Lab-2 with watsonx and watsonx Assistant
logo: docs/images/ibm-blue-background.png
---
# Refining your watsonx assistant

Before we go into all the ways to refine your first assistant, take a moment to congratulate yourself! You did it, and you finished in record time. Who would have thought that a virtual assistant capable of helping customers pay their bills or reach a live agent could be launched in under 30 minutes?

In Part 01, we created the action “I want to pay my cable bill,” plus you learned how to preview and share your first assistant so that you can immediately get your team experimenting with it AND contributing to its success.

So, now that your rocket is off and the smoke has cleared the launch site, let’s take a closer look at the payload your assistant is carrying right from the start.

On your new assistant’s homepage, we take you directly from the launch pad to mission control. Your introductory journey was aimed at learning the basics. This homepage contains all the features you’ll need to grow and strengthen your assistant over its lifecycle.

## Step 1: Enhancing your assistant

### Customize your assistant’s greeting

The first step in refining your assistant is personalizing how it greets customers.
Go to your **Actions** menu and click **Set by assistant** (under all items), then on **Greet customer**, then on the first **Conversation steps** box where you can edit the greeting to make it your own.

Some things to consider:

- Give your assistant a name that reflects your business
- Choose a greeting that describes your assistant’s purpose
- Settle on a greeting that satisfies any number of customer scenarios. For our purposes:

> "Hi, I’m Telly — Need help with your service today?”

![](https://www.ibm.com/blog/wp-content/uploads/2021/12/Customize_greeting-7.20.22-1536x821.jpg)

**Note**: Don't forget there's a "save" icon located in the upper right hand side. After changing the greeting now's a good time to use it.

### Lights, camera, more actions!

Now that your assistant has a name and a purpose, it’s time to expand the range of requests it can resolve.

In our use case, data shows that your customers want information on bundling two or more services together. That request will be your focus as you build your second action.

Go to your **Actions** menu again, but this time stay on the **Created by you** tab. Click **New action** in the top right corner, then type an example user request.

![](https://www.ibm.com/blog/wp-content/uploads/2021/12/Second_action_7.20.22-1536x837.jpg)

> I want to add a service to my plan.

As you’ll recall from building your first action, you need to train your assistant with multiple example phrases. Click the arrow in the corner of the **Customer starts with** box, then add five alternate phrases.

> How can I add a service to my plan?

> Can I bundle multiple services?

> I want to bundle more than one service.

> Bundle internet and phone

![](https://www.ibm.com/blog/wp-content/uploads/2021/12/GS-p2-Picture7.png)

Let’s define a couple of responses, since we know customers will fall into one of two categories. Go into **Edit response** and type in two options: ‘Compare pricing’ and ‘Bundle now’.

> I can help you with that! Do you want to?

![](https://www.ibm.com/blog/wp-content/uploads/2021/12/GS-p2-Picture8.png)

In the second and third steps, you’ll define conditions and assistant responses for both above options.

![](https://www.ibm.com/blog/wp-content/uploads/2021/12/TBGPII-Actions-1536x910.jpg)

> You can see a list of prices and services at [our pricing portal](https://telco.com/billing-options).

> Glad you've done your research! Let me connect you to an agent who can bundle your services!

Your assistant is now able to resolve two separate customer needs, clearly demonstrating its business value!

### Validate your steps

Human conversation isn’t perfectly predictable. There will inevitably be times when users enter responses that don’t provide the information your assistant needs. That’s why we include **Establish step validation** in the Task Tracker.

To ensure your assistant has what it needs to guide the user through an action with confidence, it will prompt the user to re-enter their response when it can’t recognize the appropriate value.

In our previous step, you defined responses for the user. If the user doesn’t select either ‘Bundle services’ or ‘Compare prices’ and instead enters irrelevant values, your assistant will prompt the user to enter a valid option. If the user continues to enter invalid options, your assistant will route the action to a fallback option (more on that later!).

Click **Edit validation** to personalize your assistant’s response and adjust the number of attempts the user gets before going to the fallback action (the number of attempts is preset to three).

![](https://www.ibm.com/blog/wp-content/uploads/2021/12/2022-07-25_12-49-50-1.gif)

Your assistant will now ask for validation from this particular step by rephrasing the options, and it will only give your users two attempts before going to the fallback option.

![](https://www.ibm.com/blog/wp-content/uploads/2021/12/2022-07-28_12-19-55-1.gif)

### Ask clarifying questions

Step validation is just one of the ways your assistant can keep the conversation going. If the customer’s request doesn’t match an action, and you haven’t singled one out for fallback, the assistant will offer default choices from among its actions.

![](https://www.ibm.com/blog/wp-content/uploads/2021/12/GS-p2-Picture23.png)

Turn this option on by clicking **Set up your assistant to ask clarifying questions** on the Task Tracker, and switching the toggle to ‘on’. You can also customize the phrasing in the **Assistant says** and **Label for a fallback choice** fields.

**Note**: These are "global" so you'll need to "x" out of the specific action you're looking at.

![](https://www.ibm.com/blog/wp-content/uploads/2021/12/Clarifying_questions_7.28.22-1536x907.jpg)

### What to do when no action matches

Your assistant is ready to support your customers with multiple tasks, but what happens when customers enter a request your assistant isn’t trained to handle yet? This is where **Retry** comes in.

Head back to the **Actions** menu, click **Set by assistant** to reveal actions preloaded into your assistant, then click **No action matches**.

![](https://www.ibm.com/blog/wp-content/uploads/2021/12/2022-07-28_11-29-08-1.gif)

Once inside, you can customize your assistant’s responses. A good strategy is to state clearly what your assistant can and can’t do. Trust us, your customers will thank you for saving them the headache.

By planning for requests your assistant *can’t resolve*, you can get your customers back on track to what the assistant *can do*.

Type example requests into the **Additional training examples** field. In this case, let’s write

> I want to go paperless

![](https://www.ibm.com/blog/wp-content/uploads/2021/12/2022-07-28_11-34-13-1.gif)

Then head over to **Conversation steps** and click the first box to edit the preloaded response as follows:

> I'm sorry, but I'm not trained to assist customers with that yet. I can help you pay your bill, add a service to your plan. Do you need help with either of these today?

![](https://www.ibm.com/blog/wp-content/uploads/2021/12/GS-p2-Picture15.png)

Finally, here’s what this example conversation would look like.

![](https://www.ibm.com/blog/wp-content/uploads/2021/12/GS-p2-Picture16.png)

### Designating a fallback action

If the assistant can’t offer the customer their desired solution, the customer may rely on your assistant’s built-in **fallback action**. Watson Assistant’s fallback action is preset to escalate to a live agent.

Your assistant will use the fallback action in three situations:

- **Agent requested** – triggered when the customer asks outright to speak to a live agent
- **Step validation failed** – triggered when the user can’t understand the customer’s request (covered above)
- **No action matches** – if you decide to forgo retry and skip directly to live agent support in your flow

![](https://www.ibm.com/blog/wp-content/uploads/2021/12/GS-p2-Picture17.png)

You can customize these responses using conditions like any other action, or you can provide different responses based on agent availability. There is even a field to provide case background to a human agent!

![](https://www.ibm.com/blog/wp-content/uploads/2021/12/GS-p2-Picture18.png)

Here’s how a simple fallback looks in the assistant preview.

![](https://www.ibm.com/blog/wp-content/uploads/2021/12/GS-p2-Picture19.png)

## Step 2: Testing and refining your assistant

![](https://www.ibm.com/blog/wp-content/uploads/2021/12/Test_and_Refine-1536x905.jpg)

### Troubleshooting and debugging

Very little can go wrong if you follow the above steps. But, you still want to double check that your assistant is firing correctly and functioning as it should.

Click **Access the preview panel and test using debug mode**. Think of this as the first in a series of short audits you’ll perform as you get closer to sharing the first version of your assistant.
Click the ladybug icon at the top left of the Preview panel to activate debug mode.

![](https://www.ibm.com/blog/wp-content/uploads/2021/12/GS-p2-Picture20.png)

This will provide a confidence score for each of the assistant’s possible responses. You can navigate directly to the step inside each action that is triggering it to make adjustments on the fly.

![](https://www.ibm.com/blog/wp-content/uploads/2021/12/GS-p2-Picture22.png)

### Optional steps: add depth to what your assistant can do

Two items on the task list are labelled **optional**. Feel free to experiment with **Create additional actions** to flesh out your assistant. We certainly did! Some examples for Telly include “I want to add a landline” and “Is my promo code valid?”.

![](https://www.ibm.com/blog/wp-content/uploads/2021/12/GS-p2-Picture25.png)

![](https://www.ibm.com/blog/wp-content/uploads/2021/12/GS-p2-Picture26.png)

The other optional task in the Task Tracker is to **Refine the assistant based on team feedback**.

### Conclusion

You’ve worked through two important steps toward getting your first assistant live. You spent under 30 minutes setting up your basic assistant, and another 30 minutes expanding on it. You now have a trusted ally that can handle multiple customer requests, and you’ve streamlined important aspects of your customer service flow. The only limit now is the sky.

<img src="https://count.asgharlabs.io/count?p=/lab2_chatbot_page">

