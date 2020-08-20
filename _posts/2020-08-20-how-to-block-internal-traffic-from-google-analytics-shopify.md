---
title: How you can block your own traffic from your Shopify store's Google Analytics
layout: post
keywords:
    - Google Analytics
    - Google Tag Manager
    - Shopify
    - web development
    - block internal traffic
    - cookies
author: Josh
---
Tl;dr:

Block yourself from appearing in your own Google Analytics data using this extension on chrome... <a href="https://chrome.google.com/webstore/detail/block-yourself-from-analy/fadgflmigmogfionelcpalhohefbnehm">Block Yourself from Analytics</a>

~~~~~~~

A commonly used method for blocking your own internal traffic is to exclude certain IP addresses or ranges using a filter in Google Analytics. This is something I've seen done at practically all the places I've worked going back a long time. I'm building a Shopify store and as it's early days and the store isn't live yet, practically 100% of the traffic at this point is me. Needless to say, I don't want to see that traffic. Those numbers will heavily skew the numbers when the site is just getting started and traffic is low.

I've got an issue though and it must be a fairly common problem for other people now that so many folk are working from home due to Covid. Since I'm using my home internet connection, I have a variable IP address. This is a very common set up for home internet users. So since I'm unable to reliably know my IP address is not changing, I needed to find another method to block traffic.

After some googling, I came across some resources for addressing this problem in a couple of ways through cookies, custom dimensions and filters. These methods relied on the use of Google Tag Manager as well as GA. Here's links to those resources which you may find useful...

<a href="https://brianclifton.com/blog/2019/11/07/filter-internal-staff-from-google-analytics/" target="_new">How do I exclude internal traffic in Google Analytics?</a>

<a href="https://www.simoahava.com/analytics/simple-way-exclude-internal-visits-google-analytics/" target="_new">#GTMTips: Simple Way To Exclude Internal Visits From Google Analytics</a>

I am doing some refresher training on GA at the moment through <a href="https://analytics.google.com/analytics/academy/" target="_new">Google Analytics Academy</a> so this was a timely chance to use the skills I was covering in the classes. I dutifully set up my custom dimension and filter in GA as well as configuring tags, triggers and variables in GTM. I was configuring all this to be served through my Shopify store.

Here's the rub... Shopify has a particular way of implementing Google analytics at the template level. You configure your analytics ID as a setting in Shopify which then gets passed to GA code in the template. You can include the GTM code snippet through the Shopify interface as well. However, it's not recommended to use GTM to send your analytics hit data. Both of the methods I found required my custom dimension to be set through this tag. This gave me problems implenmenting the cookie based solution.

I did get pretty close to get the solution working. I was able to set my cookie on a hidden internal page and then record that cookie as a custom dimension in google. But I was not able to filter myself out of the data based on the cookie.

Eventually, I found a Chrome extension <a href="https://chrome.google.com/webstore/detail/block-yourself-from-analy/fadgflmigmogfionelcpalhohefbnehm">Block Yourself from Analytics</a> that solves this exact problem. You add the extension and configure the domains you want to block. The extension handles the rest. I installed it and it's working pretty well so far. Next, how to remove all those query strings...






