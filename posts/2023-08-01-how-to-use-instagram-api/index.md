---
title: How to use Instagram API
date: "2023-08-01"
slug: /how-to-use-instagram-api
tags: ["instagram", "api"]
illustration: "pexels-sabrina-gelbart-249798.jpg"
summary: "How to use Instagram API, quick and easy."
---

## Configuration

Go to [Meta for Developers](https://developers.facebook.com/apps/) and create a new app with following settings:

- **What do you want your app to do?** Select _Other_.
- **Select an app type** select _Business_.

If you just want to access your own Instagram account, you can skip the review process. If you want to access other accounts, you need to submit your app for review.

Your application will be in _Development_ mode by default. You can switch to _Live_ mode once you are ready to submit your app for review.

Now you'll need to give access to your pages to your new app.

## Graph API Explorer

Go to [Graph API Explorer](https://developers.facebook.com/tools/explorer/) and select your app from the dropdown menu.

Select permissions for Instagram:

- pages_show_list
- instagram_basic
- instagram_content_publish
- pages_read_engagement
- pages_read_user_content

Click _Generate Access Token_ and allow access to page connected with your Instagram account.

## Get Instagram Business Account ID

Query `/me/accounts` and find page connected with your Instagram account. Copy `id` of this page.

Use this id to ask about Instagram Business Account ID `[id]?fields=instagram_business_account`.

Copy `instagram_business_account` id.

Now you can query posts for example: `[instagram_business_account]/media?fields=caption`.

Check [documentation](https://developers.facebook.com/docs/instagram-api/) for more details.
