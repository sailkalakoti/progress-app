![](https://i.ibb.co/Ks6jZc1/progress-icon.png)

# Progress

**Progress** is a simple app that creates reports based on data from chats. It can display the daily, weekly, monthly, and annual statistics.

It shows the following information:

- [Ratings](https://platform.text.com/docs/data-reporting/reports-api#ratings)
- [Chatting time](https://platform.text.com/docs/data-reporting/reports-api/#duration)
- [Response Time](https://platform.text.com/docs/data-reporting/reports-api#first-response-time)

# Preview

![progress-app](https://user-images.githubusercontent.com/74930846/218442243-58bdd7dc-bd59-46d2-ae15-e23b6c005c1d.png)

# App setup

## Before you start

To use this application in your LiveChat dashboard, you'll need to create your own app in [Developers Console](https://platform.text.com/console) and get your **Client Id**.

## Getting started

1. Go to [Apps](https://platform.text.com/console/apps) in [Developers Console](https://platform.text.com/console).
2. Click **New App** and give it an **App Name**.
3. Choose the **LiveChat** product as the product you want to build for.
4. Go to **Building Blocks**.
5. Add **App Authorization** and mark it as _JavaScript App_. Your **Client Id** will be displayed there.
6. Add `reports_read` scope to the **App scopes and API access** box.
7. Fetch the **Progress** app repository.
8. In the app directory, do the following steps:

   - Install dependencies (`npm install`).
   - In your project, go to `src/utils/congif.js` and replace `client_id` with your own **Client Id** (the one from **Step 5**).
   - Run your app (`npm start`).

9. Add your app url (for example: `https://localhost:3000`) in these two locations:

   - **Redirect URI whitelist**
   - **Agent App Widgets**

10. In **Private installation**, click **Install app**.

You should now be able to use **Progress** with LiveChat.

# How it works

[Agent App Widgets](https://platform.text.com/docs/extending-agent-app) are web applications loaded inside the LiveChat Agent App. All agents can interact with the widget during chats with customers. The widget itself is displayed in the Agent’s App right sidebar.

To get information such as **chat ratings** and **chat response time**, you need to use [Reports API](https://platform.text.com/docs/data-reporting/reports-api).

In order to pull data from our server, you need to include an **access_token** in all the requests. You can get it using [Personal Access Tokens](https://platform.text.com/docs/authorization/agent-authorization#personal-access-tokens) and [JavaScript Widget API](https://platform.text.com/docs/extending-chat-widget/#javascript-api).

You should also get familiar with [Authorization](https://platform.text.com/docs/authorization/).

# More sample apps

Experiment more with our different sample apps:
 - [Tag Master](https://github.com/livechat/tag-master) - widget for helping your agents manage tags and canned responses.
 - [Supervisor](https://github.com/livechat/supervisor-app) - widget for helping you monitor weekly progress of your agents and also their availability.
 - [Sample Redirect App with the redirect authorization flow](https://github.com/livechat/sample-app-redirect-auth)
 - [Sample Popup App with the popup authorization flow](https://github.com/livechat/sample-app-popup-auth)

# Feedback

If you find some bugs, please create an issue in this repo. We will try to fix it ASAP ;)

# [Text Platform](https://platform.text.com/): who are we?

Behind [Text](https://www.text.com/), there’s a [team of passionate people](https://www.text.com/team/) building online customer service software with online chat, help desk software, chatbot, and web analytics capabilities.

With a suite of five products ([LiveChat](https://www.livechat.com), [ChatBot](https://chatbot.com/), [HelpDesk](https://helpdesk.com/), [KnowledgeBase](https://www.knowledgebase.com/), and [OpenWidget](https://openwidget.com/)) and their powerful APIs, we power customer communication for 36,000 companies in 150 countries.

[The Platform](https://platform.text.com/) is a range of products and services that can be used to build a variety of communication tools for businesses. Our [Developer Program](https://platform.text.com/developer-program) and [Marketplace](https://www.livechat.com/marketplace/) create an open ecosystem for developers, partners, and customers. With our [advanced APIs](https://platform.text.com/) and comprehensive [documentation](https://platform.text.com/docs), you can shape the future of communication with us — starting today.

[Join our Discord](https://discord.com/invite/NcfJu3a9kM) to learn, get inspired, and meet other developers!

---

This project was bootstrapped with [Create React App](https://github.com/facebook/create-react-app).
