# What

Wordlists I use for recon and content discovery on programs from hackerone and bugcrowd. These are only things I have actually encountered in production or in documentation of popular tooling. There is no point in having a huge wordlist but only ever getting 2 hits.

# How I use these lists?

## android.txt

This is just the command I use to launch an android VM to use with MobileSecurityFramework as Geny motion is having issues with the GPU drivers I have on Linux.

## breakpoints.txt

These are commands that can be run the dev tools console of Chromium based browsers.

## burp-plugins.txt

These are some of the plugins for Burp I have installed but does not mean I have turned on at all times. I try not to rely on plugins too much as they distract you from looking at the core application.

## http.txt

I use this as my initial discovery list.  

So for example if I found an endpoint that is returning 404 for the web root.

I will use http.txt to see if there is any content there.

Sometimes I may use it recursively.

## objects.txt

I generally use this if I find some sort of API/RPC type endpoint like /api to discover the resources that the API can interact with.

## actions.txt

I use this this after discovery API objects to try map out what actions are supported.

For example say you found /api, then you found /api/account and then you run this wordlist and you find /api/account/auth

## regex.txt

You can use these in the burp suite search function, Logger++ or Highlight and Extract plugin.

## xss.txt

This is just a basic taint query I use to then trace through the application so I can easily search for "taint" and then see where it is located and which characters are escaped.

## secrets.txt

These were triggering WAFs too frequently so I split them out into their own file. Generally you are likely better off using Burps built in interesting files but this wordlist is nice and small.

## *.vmoptions files

These tune the JVM for the JRE that ships with BurpSuite. I have modified the garbage collection algorithm to use a more efficient algorithm and I have applied several graphics related tweaks.
