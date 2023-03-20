![](https://i.ibb.co/Ks6jZc1/progress-icon.png)

# Progress

**Progress** is a simple app that creates reports based on data from chats. It can display the daily, weekly, monthly, and annual statistics.

It shows the following information:

- **Ratings**
- **Chatting time**
- [Response Time](https://docs.livechatinc.com/rest-api/#chats-first-response-time)

# Preview

![progress-app](https://user-images.githubusercontent.com/74930846/218442243-58bdd7dc-bd59-46d2-ae15-e23b6c005c1d.png)

# App setup

## Before you start

To use this application in your LiveChat dashboard, you'll need to create your own app in [Developers Console](https://developers.livechatinc.com/console) and get your **Client Id**.

## Getting started

1. Go to [Apps](https://developers.livechatinc.com/console/apps) in [Developers Console](https://developers.livechatinc.com/console).
2. Click **New App** and give it an **App Name**.
3. Choose the **LiveChat** product as the product you want to build for.
4. Go to **Building Blocks**.
5. Add **App Authorization** and mark it as _JavaScript App_. Your **Client Id** will be displayed there.
6. Add `reports_read` scope to the **App scopes and API access** box.
7. Fetch the **Progress** app repository.
8. In the app directory, do the following steps :

   - Install dependencies (`npm install`).
   - In your project, go to `src/utils/congif.js` and replace `client_id` with your own **Client Id** (the one from **Step 5**).
   - Run your app (`npm start`).

9. Add your app url (for example: `https://localhost:3000`) in these two locations:

   - **Redirect URI whitelist**
   - **Agent App Widgets**

10. In **Private installation**, click **Install app**.

You should now be able to use **Progress** with LiveChat.

# How it works

[Agent App Widgets](https://developers.livechat.com/docs/extending-agent-app) are web applications loaded inside the LiveChat Agent App. All agents can interact with the widget during chats with customers. The widget itself is displayed in the Agent’s App right sidebar.

To get information such as **chat ratings** and **chat response time**, you need to use [Reports API](https://developers.livechat.com/docs/data-reporting/reports-api).

In order to pull data from our server, you need to include an **access_token** in all the requests. You can get it using [Personal Access Tokens](https://developers.livechat.com/docs/authorization/agent-authorization#personal-access-tokens) and [JavaScript Widget API](https://docs.livechatinc.com/agent-app-widgets/#javascript-api).

You should also get familiar with [Authorization](https://docs.livechatinc.com/authorization/).

# More sample apps

Experiment more with our different sample apps:
 - [Tag Master](https://github.com/livechat/tag-master) - widget for helping your agents manage tags and canned responses.
 - [Supervisor](https://github.com/livechat/supervisor-app) - widget for helping you monitor weekly progress of your agents and also their availability.
 - [Sample auth app with the redirect flow](https://github.com/livechat/sample-app-redirect-auth)
 - [Sample auth app with the popup flow](https://github.com/livechat/sample-app-popup-auth)

# Feedback

If you find some bugs, please create an issue in this repo. We will try to fix it ASAP ;)

# If you're new to LiveChat

**LiveChat** is an online customer service software with live support, help desk software, and web analytics capabilities. It's used by more than 37,000 companies all over the world. Read more about [LiveChat for Developers](https://developers.livechatinc.com/) and [join our Discord](https://discord.com/invite/NcfJu3a9kM) to learn, get inspired, and meet other developers.

---

This project was bootstrapped with [Create React App](https://github.com/facebook/create-react-app).
