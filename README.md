# What

Wordlists I use for recon and content discovery on programs from hackerone and bugcrowd. These are only things I have actually encountered in production or in documentation of popular tooling. There is no point in having a huge wordlist but only ever getting 2 hits.

# How I use these lists?

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
