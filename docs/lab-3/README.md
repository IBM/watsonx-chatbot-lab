# Deploying watsonx assistant 

You built your first action with Watson Assistant in Part I, then refined your content in Part II. Now let’s learn how to test your assistant and deploy it on your website! 

## Publish and preview your assistant’s content 

Go to the **Task tracker**, click the arrow next to **Deploy your assistant to a test channel**, then select **Publish your latest content to the live environment**.  

![](https://www.ibm.com/blog/wp-content/uploads/2022/01/Publish_etc-1536x911.jpg)

Click the blue **Publish** button at the top of the table, and voila: you’ve published your first version of your assistant’s content! Your assistant is not visible to customers yet (we’ll cover that process soon), but this version is preserved, and any subsequent edits you make will be saved in the draft environment. 

![](https://www.ibm.com/blog/wp-content/uploads/2022/01/Publish_rocket-1536x762.jpg)

Now it’s time to share this first version of your content with your colleagues! Click the **Preview** icon (the play icon) to open up the Preview page.  

![](https://www.ibm.com/blog/wp-content/uploads/2022/01/2022-07-26_14-55-30-1.gif)

The left-right navigation has three key links: 
- Change background website – click this button and type/paste your organization’s URL to make your homepage the background behind the chat panel 
- Copy link to share – click this button to copy the Preview URL to your clipboard, then forward it to your team 
- Customize web chat – this button takes you to the web chat editor where you can personalize your chat panel’s elements 

Your colleagues are your best resource for refining your assistant’s content: they know the business, your customers’ pain points, and what questions most frequently need answering.  

### Best practices we’ve identified for testing your assistant: 

- Send the preview link to 10-15 colleagues 
- Don’t invite anybody who was part of the building process  
- Ask your colleagues to spend 10 minutes interacting with the assistant 
- Ask them to log and categorize any issues they had 
- Instruct your testers to ask for a human agent if they get frustrated  
- Make sure you collect at least 20-30 conversations 

When reviewing conversation logs and your colleagues’ notes, the two main areas to focus on are:  

- **Understanding**: Is your assistant properly understanding user requests? Are there frequent topics that you haven’t trained your assistant to handle yet?  
- **Resolution**: Are users successfully completing actions? Is the assistant escalating actions to human agents more frequently for certain actions? 

You can review the details of each conversation in the **Conversations** tab of your assistant’s **Analyze** page (we’ll give you a tour of that page later). Reviewing conversations is an ideal way to improve your assistant’s actions. Once you deploy your assistant to your customers reviewing every conversation will be unrealistic, so take advantage of this early testing phase to rigorously refine your assistant’s actions. 

## Customize the web chat

The web chat channel integration is automatically included with every instance of Watson Assistant. Click **Customize web chat** on the Preview page or select Web chat on the home page to open the web chat editor.

![](https://www.ibm.com/blog/wp-content/uploads/2022/01/2022-07-27_10-22-41-1.gif)

**Style**, the first tab on the page, lets you name your assistant, adjust the text bubble and header colors, and add your company’s avatar (you’ll need to upload your avatar image to a URL to do this).  

![](https://www.ibm.com/blog/wp-content/uploads/2022/01/2022-07-27_10-27-19-1.gif)

**Home Screen** is where you can edit your assistant’s initial **Greeting** to the user. As the page states, “Good greetings are welcoming, actionable, and expressive of your assistant’s personality.” 

Once you’ve got a greeting that you’re happy with, add **Conversation starters** in the field below. These conversation starters should be simple phrases that match your assistant’s actions. They appear in the chat panel above the user input field.

![](https://www.ibm.com/blog/wp-content/uploads/2022/01/WC_Home_Screen_7.28.22-1536x907.jpg)

When the user selects an option from among the starters, your assistant automatically funnels the user into the appropriate action — no heavy lifting required!

The web chat editor is also where you configure **Suggestions**. Suggestions are automatically configured **on** when you create your assistant. Suggestions appear in the chat panel when your assistant receives a request it doesn’t recognize. They’re designed to funnel the user into an action, just like the Conversation starters. 

![](https://www.ibm.com/blog/wp-content/uploads/2021/12/Picture7.jpg)

The option label is preloaded with **Connect to an agent**. This option appears when the user clicks on the **?** icon in the corner, or after three failed attempts (refer to Part II for more info on this feature).  

## Get acquainted with your assistant’s analytics

Your assistant collects data from conversations with users in both the draft and the live environments. Once customers start interacting with your assistant, the Analyze page starts capturing data. This data will guide you as you continuously refine your assistant based on its success in resolving users’ requests. 

Select **Get acquainted with your assistant’s analytics** in the Task Tracker or click the chart icon to go to Analyze. 

![](https://www.ibm.com/blog/wp-content/uploads/2021/12/Picture8.jpg)

You have the option to view analytics from a fixed date range (just open the dropdown menu and select a range) or to view a custom range based on specific dates.  

The centerpiece of the Analyze page is the **Completion and Recognition** tables. The data in these tables show you how often your assistant can successfully guide users through the end of an action, and how often it recognizes user requests. Beneath the tables, you’ll see lists of most frequent actions, least frequent actions, and least completed actions. 

The **Conversations** section lets you view actual interactions between end users and the assistant. You won’t need to guess what’s working and what isn’t, because you’ll have data tracking built into your assistant’s payload, plus real-world examples of interactions between your assistant and its users. 
Once you’ve taken the tour of the analytics and you’re ready to make use of it, take a moment to congratulate yourself: you’ve reached “the end of the beginning” and have an assistant that’s ready to meet your customers! 

## Deploy your assistant

There are two short steps left before your customers can chat with your assistant on your website:

### 1. Publish your latest content and assign it to the live environment

Return to the **Publish** page by clicking the rocket icon on the side menu, or by clicking **Publish your latest content to the live environment** in the Task Tracker. You’ll see a list of all the edits you’ve made since publishing V1 in the table. Click the blue **Publish** button to publish V2 of your content. 

**Note**: *We cover publishing, the two-environment structure, and lifecycle management in more depth in Part 04*.

To assign V2 to the live environment, go to your **Environments** page, click **Assign a version**, then select V2 in the modal. 

![](https://www.ibm.com/blog/wp-content/uploads/2022/01/Assign_version_7.27.22-1536x907.jpg)

Again, every time you publish a version of your assistant, you create a snapshot of your current content. The version assigned to the live environment will be the one your customers interact with, and any new content you add to your assistant will be saved in the draft environment until you’re ready to publish it as a version.

### 2. Deploy your assistant on a live channel across a broader set of customers.

When you’re ready to launch your assistant on your website, it’s literally as easy as copy and paste! Return to the web chat editor and click the **Embed** tab. 

You’ll see the JavaScript code snippet you’ll need to integrate your assistant into your website. Click the copy icon next to the script, open the HTML source for any page on your website, and paste the snippet in.  

**Pro Tip**: Paste the snippet as close to the closing </body> tag as possible to ensure that your page renders as fast as possible. Refer to the documentation for the new Watson Assistant to get the deepest dive possible on deploying your assistant to your website. 

![](https://www.ibm.com/blog/wp-content/uploads/2021/12/Picture11.jpg)

Not only is your assistant now live and ready to start answering customers’ questions, you also have the option of deploying your assistant on as many of your site’s pages as you want. Just make sure you only add the code snippet once per page. 

## Success! Now the fun begins

![](https://www.ibm.com/blog/wp-content/uploads/2022/01/Task_tracker_complete-1536x913.jpg)

You now have a virtual agent live on your website, built, tested, and deployed in less than an hour!  
As great as this first version of your assistant is, you’ve only scratched the surface of what it can do. 
