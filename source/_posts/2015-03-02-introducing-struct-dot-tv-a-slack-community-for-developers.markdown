---
layout: post
title: "Introducing Struct.tv a slack community for developers"
date: 2015-03-02 20:34:33 -0600
comments: true
categories: 
  - news
---

## Why slack?

When choosing the platform for our new community we evaluated a number of solutions.  We considered everything from building a custom solution to trying to roll something out using Wordpress.

In the end we landed on a bit of a hybrid. 

The core of our community is driven by slack. Slack is a real time chat application that runs on any system from native mobile and desktop apps to a first class web app that runs in your browser. 

The great thing about slack is that it allows us to write our extensions via their api. So far we've developed a help system that has allowed us to hack slack into a stackoverflow-esque platform.

## Help System

To ask for help with ruby, simply join the __#ruby-on-rails__ channel and type `/helpme I need help getting carrierwave to work with amazon s3` . This will post your issue to http://struct.tv/help_requests , announce your issue to the channel and place you in a new chat room specific to your issue. If people want to help they can join the room and you can work to a solution while avoiding the noise of the chat channel.

## Easy Screen sharing / Remote Pairing with Screenhero

Slack recently purchased screen hero and made it free for all slack users. To use slack to remotely diagnose a problem, or pair with another developer simply have Screenhero open on both computers and type `/hero @username` to connect with another user.
