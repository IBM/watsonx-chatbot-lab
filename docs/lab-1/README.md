# Getting started with watsonx Assistant part I: the build guide

Chatbots are a great way for you to naturally and efficiently help your customers get stuff done, but most chatbot building tools today are either overly simplistic and break whenever someone asks your bot something unexpected, or focused only on a developer as the bot builder, making it very hard for content-focused individuals to collaborate.

![](https://www.ibm.com/blog/wp-content/uploads/2021/12/Picture2-1.png)

We think it’s about time a bot-building tool let anyone build robust AI-powered bots: bots that can automatically handle the craziness of human conversation and scale across a company without breaking.
That’s why watsonx Assistant has a build experience tailored to the people who directly interact with customers daily.

![](https://www.ibm.com/blog/wp-content/uploads/2021/12/Picture3-1.png)

You don’t have to sacrifice on powerful chatbot features either. watsonx Assistant will automatically handle all sorts of things that could go wrong during a conversation, such as topic changes, vague requests, misunderstandings, and asking for a human agent.
In this post, we’ll show you how to create a fully-built action in your new assistant in 30 minutes or less. Here’s what you’ll do:

1. Learn the basics (5 min)
2. Create your first assistant (5 min)
3. Create your first conversation (15 min)
4. Preview your assistant (5 min)

## 1. Learn the basics (5 min)

Actions and steps are the only two things you need to know to build an AI-powered virtual agent.

![](https://www.ibm.com/blog/wp-content/uploads/2021/12/Picture4-1.png)

### What is an action?

An action is a problem or a task that your customer wants to resolve. Anything from paying a bill to getting an invoice to saying hello to asking about the weather could be an action in your assistant.

![](https://www.ibm.com/blog/wp-content/uploads/2021/12/Picture5-1.png)

### What is a step?

A step is just a back-and-forth interaction between your assistant and your customer.
Simply put, steps represent the clarification questions, final answers, or human agent handoff points in the action.
Everything else that the step needs to function like the flow logic, response options, or storage of the user’s response is contained within the structure of the action itself. You no longer need to create separate entities and intents as part of a dialog skill!
In the example above, the assistant asks clarification questions before handing the conversation over to an agent (with the account number as context) to pay a cable bill, or guides the user to the online billing portal for internet or phone bills.

!!! tip
    If you’re an existing watsonx Assistant customer, we have a convenient way for you to use dialog and actions together in the new product experience by downloading and migrating your dialog skills! You can do this gradually over time to gain the advantages of important new features in actions while maintaining the work you’ve built into your classic assistant.

## 2. Create your first assistant (5 min)

When you first launch the watsonx Assistant experience, you’ll be prompted to create your first assistant:

![](https://www.ibm.com/blog/wp-content/uploads/2021/12/Picture8-1.png)

Give it a name that represents the domain of topics you want it to handle. For example, if you are building an assistant to handle support questions in your billing department, you might start by calling it the “Billing Assistant.” Choose what language you want it to speak before continuing. Watson Assistant can handle virtually any global language.

!!! tip
    If you haven’t already thought about what you want your assistant to handle or where it will talk to your customers, check out our post on planning your assistant. You can also take advantage of one of the templates in our catalog for your first assistant. This will dramatically reduce your timeline, as well as teach you the ropes.

From here, you’ll start on the home page of your brand-new assistant:

![](https://www.ibm.com/blog/wp-content/uploads/2021/12/Picture9.png)

You’ve already done the first two steps, so take a moment to check out what’s on your screen. Each section is organized with progress bars so you can see what you’ve done and how far you have to go.

In the top right of your screen you’ll also find the Learning center. Click to expand and open the menu items to find tours, shortcuts to useful content, and more. All of this is aimed at getting you up and running as quickly as possible, so be sure to explore.

Now it’s time to build your first conversation. Follow along with our example or create your own!

## 3. Create your first conversation (15 min)

Let’s build out a conversation flow using our billing example from before:

![](https://www.ibm.com/blog/wp-content/uploads/2021/12/Picture10-1.png)

For an internet or phone bill, the customer will be sent to the online billing portal.

For cable bills, our fictional company’s policy dictates that a human agent has to take payment. In this case, the assistant needs to get the customer’s account number first to speed things up with the human agent.

Let’s build it!

### Create your first action

Start by creating your first action. Remember that actions represent the topics your assistant can handle, such as “pay bill.”

!!! tip
    You will be prompted to create your first action from scratch or from a template. To follow along with our example you’ll want to choose the first option, but we definitely recommend exploring the templates at your disposal as you build out your proof of concept. You’ll find a number of options that are customer-ready, or that can expand on your first assistant’s abilities.

![](https://www.ibm.com/blog/wp-content/uploads/2021/12/Picture11-1.png)

### Create your first example

You need to “train” your assistant’s topic-recognition AI by giving it some example sentences. Start with the first one here, something like: I want to pay my cable bill please.

![](https://www.ibm.com/blog/wp-content/uploads/2021/12/Picture12.png)

### Create your first step

Now it’s time to create the first step in the bill pay interaction. We’ll start with the clarification question around the customer’s account type:

![](https://www.ibm.com/blog/wp-content/uploads/2021/12/Picture13.jpg)

Step 1 was already created for you, so move to it and add the clarification question in the Assistant says text box. Something along the lines of: **What type of account are we talking here?**

![](https://www.ibm.com/blog/wp-content/uploads/2021/12/Picture14.png)

Then, select the type of customer response the assistant should wait for. In this case, options are the best choice. Add the three options for Cable, Internet, and Phone, and apply your changes.

![](https://www.ibm.com/blog/wp-content/uploads/2021/12/Picture15.png)

Your first step should ultimately look something like this:

![](https://www.ibm.com/blog/wp-content/uploads/2021/12/Picture16.png)

### Preview your action

Now preview your action to make sure it works. To do this, hit the preview button in the bottom right corner of your screen. Try out a few interactions and see that it properly recognizes what you ask it. Try typing something other than your earlier training sentence.

![](https://www.ibm.com/blog/wp-content/uploads/2021/12/Picture17.png)

### Create another clarification step

With your first step created and tested, let’s finish this action by creating another step. As a reminder, we still need to build steps 2, 3, and 4:

![](https://www.ibm.com/blog/wp-content/uploads/2021/12/Picture18.png)

Let’s add step 2 next. Add a new step below step 1:

![](https://www.ibm.com/blog/wp-content/uploads/2021/12/Picture19.png)

Next, add the clarification question asking for the account number. Something like: **What’s your account number?**

After you’ve done that, you need to tell the assistant to look for a number in response to the question. From the response dropdown list, choose **number**:

![](https://www.ibm.com/blog/wp-content/uploads/2021/12/Picture20.png)

Next, you need to add some flow logic. Remember, given the way this flow works, an account number should only be gathered in the case of a cable bill. To handle this scenario, you need to add a condition to your step. To do that, change the step to be taken **with conditions** instead of **without**:

![](https://www.ibm.com/blog/wp-content/uploads/2021/12/Picture21.png)

Conditions are requirements which must be met for the step to be triggered. In this case, we want to condition on the answer to step 1 being **Cable** but not **Internet** or **Phone**. Setting this up is easy. Just make sure you have the condition set to step **1 is Cable**:

![](https://www.ibm.com/blog/wp-content/uploads/2021/12/Picture22.png)

Once you’re finished setting the condition, your action should look something like this:

![](https://www.ibm.com/blog/wp-content/uploads/2021/12/Picture23.png)

### Create an agent handoff step

You’re almost finished building this action! We just need to add steps 3 and 4, each of which provide the final outcome for the user:

![](https://www.ibm.com/blog/wp-content/uploads/2021/12/Picture24.png)

Let’s start with step 3. Add it below step 2 and add some text related to getting the user to an agent to pay their bill. Something like: **Let me get you to an agent who can help you pay your cable bill!**

![](https://www.ibm.com/blog/wp-content/uploads/2021/12/Picture25.png)

Next, condition this step on step **1 is Cable** just like you did in step 2:

![](https://www.ibm.com/blog/wp-content/uploads/2021/12/Picture26.png)

Finally, for this step, we don’t need to gather any information from the user, so you can leave the **define customer response** section empty.

We should, however, set up the assistant to route this conversation to a human agent. To add that, change the **and then** setting to connect to a human agent (which will also end the action when it hands off):

![](https://www.ibm.com/blog/wp-content/uploads/2021/12/Picture27.png)

In the prompt that comes up, you should insert the context that you gathered for the human agent to review. Namely, the fact that the customer wants to pay their cable bill as well as the account number.

!!! tip
    To insert the information To insert information you’ve collected into text, start with the **$** sign, and a quick select box should appear like this:

![](https://www.ibm.com/blog/wp-content/uploads/2021/12/Picture28.png)

Select step 2 (the account number) as the field you want to insert and apply your changes.

Step 3 should be complete and look like this:

![](https://www.ibm.com/blog/wp-content/uploads/2021/12/Picture29.png)

### Create a final response step

Lastly, add step 4. It should say something like: **To pay your \<type of bill\> bill, you can head to our online portal \<link to portal\>**

To insert a variable like the type of bill being paid, click the variable insert button at the top of the text box:

![](https://www.ibm.com/blog/wp-content/uploads/2021/12/Picture30.png)

And to add a link to the text, highlight the text you want to use and then click the link button:

![](https://www.ibm.com/blog/wp-content/uploads/2021/12/Picture31.png)

The settings for the link should look something like this:

![](https://www.ibm.com/blog/wp-content/uploads/2021/12/Picture32.png)

Next, make sure this step only fires for an internet or phone bill. To do that, create a condition for **step 1 is Internet**. Then add another condition for **step 1 is Phone**. When you do this, be sure that the step looks for **any** of these conditions to be met and not **all** of them:

![](https://www.ibm.com/blog/wp-content/uploads/2021/12/Picture33.png)

Finally, make sure the action ends after this step is reached. To do that, change the **And then** setting to **End the action**.

![](https://www.ibm.com/blog/wp-content/uploads/2021/12/Picture34.png)

Test the whole action
Boom! Your steps should now be complete and look like this.

![](https://www.ibm.com/blog/wp-content/uploads/2021/12/Picture35.png)

Now for the fun part, let’s try it out!

![](https://www.ibm.com/blog/wp-content/uploads/2021/12/Picture36.png)

Try a few scenarios where you state the type of bill up front. Notice how the assistant skips that question and moves immediately to the next step.

![](https://www.ibm.com/blog/wp-content/uploads/2021/12/Picture37.png)

Add some more examples
You may notice when testing that the assistant doesn’t correctly recognize everything you ask it. To address this, you need to train the AI with more than just one example sentence. Simply move to the top of the action in the customer starts with section and add four more varied sentences:

![](https://www.ibm.com/blog/wp-content/uploads/2021/12/Picture38.png)

!!! tip
    While you’re at it, we recommend naming your action (top left of the image above) with something simple that your customers would recognize. In this case, maybe something like “Pay a bill.”

## 4. Preview your assistant (5 min)

To see how your assistant would work on one of your channels, head to the preview page:

![](https://www.ibm.com/blog/wp-content/uploads/2021/12/TBGP1-Preview-Page-1536x916.jpg)

This page is a representation of your “draft” work in progress. It has an inline preview for you to test. You can also share your work with others on your team quickly with a shareable URL:

![](https://www.ibm.com/blog/wp-content/uploads/2021/12/TBGP1-Preview-Page-1-1536x916.jpg)

Simply click that button to copy the URL to your clipboard, then paste it into any messaging service to share your draft with members of your team.
The embeddable web chat integration is included for you by default, and you can go to the integration catalog to add any other channels to your assistant, such as phone integration:

![](https://www.ibm.com/blog/wp-content/uploads/2021/12/TBGP1-Preview-Page-2-1536x964.jpg)


Congrats! You’ve successfully learned all you need to know to get started with watsonx Assistant. From here, start building out the topics you really care about automating with your customers.
