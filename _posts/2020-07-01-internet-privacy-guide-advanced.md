---
layout: post
title: Advanced Internet Privacy Guide
category: internet, privacy, advanced, guide
date: 2020-07-01
---

This is very detailed guide on how to protect your privacy online and be as most anonymous as possible. This guide is for almost anyone, from people who want to avoid being tracked online to the most very paranoid.

Remember: *Big Brother Is Watching You*

## Smart People...

**Disable JavaScript**

Use Privoxy to disable JavaScript FOR REAL and do not trust their browser or add-ons to do this simple fucking task.

Always get the latest version of [default.filter](https://www.privoxy.org/gitweb/?p=privoxy.git;a=blob_plain;f=default.filter;hb=HEAD) for Privoxy

Disable WebSockets and WebRTC when using Tor. The next dangerous garbage to look out for will be WebAssembly. *hint: about:config wasm*

Use Anti-Malware And Keep That shit Up To Date.

Browse in Firefox to **about:about** then click on Telemetry and turn that shit off.

[Disable Windows 10 Telemetry](https://www.oo-software.com/en/shutup10)

Do Not Browse Web On SuperUser / Admin Account.

Use Private Browsing Tabs Per Site.

Encrypt Their OS Disk and Virtual Machine Disks.

Copy / Paste their password from their vault FIRST, then their username, to keep password out of copy buffer. *Hint: JavaScript and even CSS tricks in some browsers can steal this.*

DO NOT talk to cops. They get lawyers and refuse to talk to anyone except their lawyer they paid for. they would never trust a "public defender". TIP Find a reputable law firm with a high success rate that has a toll free number. Pre-Pay (retain) them and **memorize** their toll-free number, as your phone will be taken away. If you are thrown in a holding cell, it will have a shit barely functional "phone" that has just a keypad and a shit speaker, no handset. The numbers of lawyers in the cell are intentionally BAD lawyers the cops know will lose and put you into debt. Call YOUR lawyers toll-free number, tell them your name, what you are accused of and where you are. That's it, nothing more! Do not say you can not afford this. Buy one less stupid thing, one less new shiny thing.

Do not assume they are guilty. They shut the fuck up and let their lawyer do all the talking. They ignore the mind games that cops will play with them. That is their job, to fuck with your head and force you to admit to shit. You will not win at their game, so shut the fuck up, demand to see your lawyer! If they keep playing, then demand to see internal audit and your lawyer! Do not say anything. Do not sign anything.

DO NOT go at it alone. If you have a group of friends that share the same ideas, beliefs, vision as you, then form a brotherhood, sisterhood that invokes zealous pseudo-religious principals so that if one of you is attacked, everyone attacking is attacked 10,000,000 fold. This is how every "protected" group invoke self protection. Some example are feminists, PETA©, vegans, religious fundamentalists (emphasis on mental), political wingnuts, environmentalists (also emphasis on mental).... and so on. If your friends have not formed such a bond and let the world know how "**fuCkiNG bAtshit CrAzY**" your massive group is, then you are all alone, Mr. Potter.

Know that where lawyers fail, time based countermeasures must kick in. Research "Mutually Assured Destruction"

## Paranoid People...

**Do Not Mix Social Media And Dark Web**

install their browser with the internet disconnected and exit after installing. *Do not "Run Now" since you were installing as Administrator, duh.*

Pre-configure Firefox with the internet disconnected.
- Create and edit the file:
```
%APPDATA%\Roaming\Mozilla\Firefox\Profiles\*.default\user.js
```
- Use [this template](https://github.com/pyllyukko/user.js/blob/master/user.js) as a starting point. Read through it and edit manually. Any part you do not understand, read up on it.
- Create and edit the file
```
%ProgramFiles%\Mozilla Firefox\distribution\policies.json
```
- With the following
```
{
     "policies": {
      "DisableAppUpdate": true
     }
 }
```
- All of this will be deleted every time you manually update Firefox.
- Back up the user.js and policies.json and create a script that will always put it back before firefox is started.
- [Further Reading](https://unixsheikh.com/articles/mozilla-is-becoming-evil-be-careful-with-firefox.html) on how even Firefox is losing touch. It is still significantly safer than Chrome and all the chromium variants.

Increase the DNS TTL in about:config to reduce some tracking. Know that JavaScript can send your IP addresses, both private network and public IP of your home, via a DNS request. Even if you proxy DNS through SOCKS, people can see your REAL IP in their DNS query logs.

Check for browser leaks in both [BrowserLeaks](https://browserleaks.com/) AND [IP Leak](https://ipleak.net/)

Use [Privoxy](https://privoxy.org/)+[Squid](http://squid-cache.org/)+[Tor](https://torproject.org) on a remote hardened system over a VPN. Squid must only use memory cache and not disk cache. Restart Squid and defrag memory to erase its contents when not in use. Configure Squid to force high cache-control times on static content. On a remote hardened systems means that even Tor does not know where you originated from.

Did you know ... I can tell what operating system you are using from your first SYN packet?  
If you are not at least using privoxy from a generic Linux host, then I can tell if you are on:  
Win7 Win10 Linux Androiod iPhone Mac ... all of this from your very first SYN packet using eBPF.

To stop people from seeing this, use Browser -> VPN -> Squid -> Privoxy -> Tor
- A [VPN](https://github.com/StreisandEffect/streisand) keeps Tor traffic off your home network.
- Squid caches Onion sites to make them faster.
- Squid gives you POWERFUL control over content behavior.
- Privoxy gives EXTRA control over content behavior.
- Tor is just a Proxy that uses onion routing.

Browse Web From Virtual Machine On Encrypted Volume. *VeraCrypt, BestCrypt, dm-crypt*

Boot their OS entirely into RAM and then use 100% of the block devices for encrypted storage.

Know that most VPS providers can live migrate and backup your VM, read all memory and encrypted disk contents, without your knowledge.

Limit *WHEN* Their Anti-Malware And Other Programs May Dial Home.

Know that anti-malware programs can be configured to log and REPORT files that are known to be illegal.

WAIT for a couple minutes for Anti-Malware and Anti-Virus to ACTUALLY start up all the way before connecting to the internet.

Use App and Network Firewalls To Block Non-Tor When Using Tor.

Use Browser Addons To Change User-Agent **Per Domain**. *...but it will make me unique* **Lies! you already are.**

Use Browser Addons To **Disable Javascript And CSS ExFil**.

Disable the addons bundled with their browser, such as **screenshots** which can be triggered remotely by skiddies to grab screenshots of **your screen** and steal your shit. *about:config screenshot*

Do not use cloud storage for their passwords. *Oh, your vault is encrypted with WHAT password? lol*

Do not use cloud single sign-on vendors, duh.

Do not sign into a site using Facebook, Google, Microsoft, Apple

[Hide their text](https://github.com/rw/plainsight/) using stenography and PLAIN text.

Clean Their Encrypted Volumes With [CCleaner](https://ccleaner.com/ccleaner), [BleachBit](https://bleachbit.org/), [BCWipe](https://jetico.com/data-wiping/wipe-files-bcwipe) as **non-admin** for **user** shit

Clean Their Encrypted Volumes With [CCleaner](https://ccleaner.com/ccleaner), [BleachBit](https://bleachbit.org/), [BCWipe](https://jetico.com/data-wiping/wipe-files-bcwipe) as **admin** for **system** shit

*Too hard? What commands might you wished you had run when you find your equipment confiscated.*

Add **Many** Encrypted File Based Volumes On Top Of Their Encrypted OS Disks, Including Dummy Volumes, With Retardedly Long Passphrases That One Can Not POsSiBlY Type Whilst Drunk. *See VeraCrypt, BestCrypt, dm-crypt*

Do not say much on *The Dark Web* to avoid their writing style being mapped to their *Clearweb* identities. As mentioned on [ni-chan](http://plnemlsyla6h5t3nuoz2algzmy635ceuendnjwsmhwn2os5fxahshiad.onion/) this is _[stylometry](https://wikiwand.com/en/Stylometry)_, the study of someones writing style, that can be used to identify them. Exceptions are those that can intentionally write in vastly different and random styles with random intentional misspellings, such as this page. Be sure to mix in phrases and slang terms from dozens of cultures and regions mate. Add intentional misspelling that is unique to each site.

Are heavily armed, have class 5 armor to wear, have safe underground rooms, plenty of food and water and medical supplies, have multiple underground filtered insulated thick pipes to provide fresh air from far away from multiple directions. Most important, plenty of storage or transport of piss and shit. Save the piss and shit for your attackers. Get high volume pumps to cover your attackers in piss and shit. Build fake shelters to distract from the real ones. Use tunnels to inter-connect some shelters. Add intercom to use computer voice to chat with your attackers. They must instantly see it will cost them millions or billions of their budget to attack you. You MUST start the mind games with them before they have the chance to start them with you. Look up Psychological Warfare.

Stay Clear Of Warrantless Lawful Intercept Products And Services Such As:
- 4chan
- ~~8chan~~ R.I.P
- Amazon AWS & Alexa
- Apple & Siri ([FBI Uses Greykey To Unlock iPhone 11 Pro Max](https://www.macrumors.com/2020/01/16/fbi-used-graykey-to-unlock-iphone-11-pro/))
- AT&T
- CloudFlare ([CSAM Reporting](https://blog.cloudflare.com/cloudflares-response-to-csam-online/))
- Discord ([Saves Everything Forever](https://blog.discordapp.com/how-discord-stores-billions-of-messages-7fa6ec7ee4c7?gi=3ec4badcbc4a))
- Facebook
- Google
- Microsoft
- PlayStation
- Slack
- Snapchat
- Steam
- Verizon
- Xbox & Cortana
- Yahoo
- YouTube

**IF YOU ARE NOT RUNNING THE SERVER :: YOU ARE BEING MONITORED AND RECORDED**

**IF YOU ARE NOT RUNNING THE SERVER :: CHAT LOGS WILL BE SAVED FOREVER AND MAY BE USED OUT OF CONTEXT TO HARM YOU**

You can run your own text and voice chat servers. Teamspeak, Mumble, IRC and probably many others. If **you** are not running the server, someone else is. Do you trust them to not use your words against you? Do you trust them to not share your private conversations? Use plugins / addons in IRC to implement End-To-End encryption like OTR also known as "Off The Record". Even IRC servers have modules that allow admins to capture private chats. Encrypt your private chats end to end with OTR.

You can also encrypt files using openssl and changing which cipher and passphrase is used based on the day of the week, number of week of the year, or Julian date (day). Create a table that has 365 long passphrases and 365 ciphers. Or 52 (one for each week) if one per day is too complex.

**TL;DR** Instead of Discord, consider Mumble or Teamspeak. Instead of WebEx/Zoom, consider self hosting Jitsi.

Facebook and Google have Tor sites. Logged into FB or Google? Your creds can be exfil to .onion to ID you on Tor.

Notice some chans have a poster ID, thread ID? Mix in a key and reverse everyones IP, lulz. Easy mode for LE.

And seriously 8chan, allowing YouTube to be embedded in a chan? WTF, LOL. Instant tracking of any clown logged into Google or YouTube.

It is **EASY** to put your videos on your own site and link to them on other sites. YouTube can not take down videos that they are not hosting.

*We are anonymous* ... lol, not if you are logged into YouTube or Google or Gmail or any of the Alphabet DARPA / Stanford SRI / Harvard products.

---

**Beware of people Doxxing users with ZeroNet.**

ZeroNet Is **NOT** Anonymous.

---

Enable JavaScript on ClounFlare? Logged into Gooogle or YouTube? You are being doxxed!

There also be people that will pretend to sell big pharma products. **Ignore them**, they are trying to get your mail route and trick you into giving them virtual currency. They be **scammers**, victim beware.


If someone is posting magnet torrent links, they are trying to **dox** you.

[Here](https://www.coindesk.com/us-law-enforcement-traces-bitcoin-transactions-to-nab-largest-child-porn-site) is an example of people getting doxxed by using virtual currency and somehow thinking it is in any way anonymous.

Intercept DNS traffic to ports 53 and 853 and route it through their own DNS proxy using either DNSCrypt or a VPN tunnel to other DNS recursive servers to reduce some visibility by their ISP for non Tor traffic. To hide the remaining traffic, one can attempt to use a VPN when feasible. Know that VPN providers can see your traffic, so consider running your own VPN. See [Algo](https://github.com/trailofbits/algo) or [Streisand](https://github.com/StreisandEffect/streisand). Try to find ways to make anonymous payments to server hosting providers. If renting a physical machine, use OpenIPMI to change credentials on the remote management card and update the firmware.

Never route their DNS through ClounFlare or any other commercial ent-titties. It will not be long before your browser is doing this without your knowledge! Look in Firefox about:config for **.trr.** Set **network.trr.mode** to **5** to disable that shit **or** change the **network.trr.resolvers** to point to your own DoH DNS server. Those stinky shady cunts are doing this under false pretense. Warn your family members and all loved ones about the attack on your privacy.

Never route any of their DNS traffic to CloudFlare or any of the other dumb DoH centralized DNS tracking sites. Instead set up your own DoH server for your friends and family to use, then you can see how much tracking CF can do.

Power Off Their "Smart" Phones and Obliterate Alexa.

Seriously, fuck Alexa and Siri in "their" spy holes.

Let's give spy devices human names and genders so we allow them to listen to us. herp derp

Let's pay for GPS trackers and use basic psychology to get people to keep them on 100% of the fucking time.

Let's connect every fucking device to some rando's *cloud* because we are too fat and lazy to get up to unlock the door.

By the way, removing your SIM card from your cell phone does NOT make you anonymous. The IMSI number from your SIM is mapped to your IMEI number from your cellphone. Both can be tracked and both are mapped to you after the first time you use your SIM card.

As mentioned in, also beware of game platforms spying on you. Valve's Steam can be used to watch and record your desktop without your knowledge. Xbox's Cortana is just like Alexa and Siri. Cortana and other console game spy applications can monitor and record everything you and your family are saying. Automated transcription can trigger off keywords and phrases to alert the authorities that you are speaking ill of someone or something or talking about a sensitive topic. These recordings can also be used in some courts to prosecute you as evidence. As the propaganda posters from WWII said, "Loose Lips Sink Ships". I miss those posters.

Most modern televisions ARE spying on you. If you connect your TV to Wifi or if there is an unprotected WiFi near by, the TV will auto-connect to it and exfil your conversations, images of you and your family to companies doing Machine Learning. This data is often NOT protected and left unsecured in Amazon AWS S3 buckets. This is not by mistake. This allows them to sell leak your data and have plausible deniability about how others obtained this data. This data is acquired by anyone with enough money. Resellers provide this data to law enforcement, so they can watch you in your home without a warrant and listen to anything you say.

Do not let things stress them out. Stress raises cortisol levels and makes you weaker and more vulnerable to disease. Divert or redirect all of your stress to others. Let other people stress for you. The concept is called Shared Pain. Redirect the stress from others back onto them 10 million fold.

## Suggested Browser Addons
- [Clear Cache](https://addons.mozilla.org/en-US/firefox/addon/clearcache/)
- [Cookie AutoDelete](https://addons.mozilla.org/en-US/firefox/addon/cookie-autodelete/)
- [CSS ExFil Protection](https://addons.mozilla.org/en-US/firefox/addon/css-exfil-protection/)
- [CSS Override](https://addons.mozilla.org/en-US/firefox/addon/css-override/)
- [FoxReplace](https://addons.mozilla.org/en-US/firefox/addon/foxreplace/)
- [Disable WebRTC](https://addons.mozilla.org/en-US/firefox/addon/happy-bonobo-disable-webrtc/)
- [NoScript](https://addons.mozilla.org/en-US/firefox/addon/noscript/)
- [Privacy Badger](https://addons.mozilla.org/en-US/firefox/addon/privacy-badger17/)
- [Privacy Settings](https://addons.mozilla.org/en-US/firefox/addon/privacy-settings/)
- [uBlock Origin](https://addons.mozilla.org/en-US/firefox/addon/ublock-origin/)
- [User-Agent Switcher](https://addons.mozilla.org/en-US/firefox/addon/uaswitcher/)

Old versions of NoScript can be bypassed using the content type **Content-Type: text/html;/json**

If disabling Javascript "Breaks A Website", the website was already broken by design.

There is NO reason for a chan site or public forum to require JavaScript, ever!

If your IP gets blocked, go to an open Wifi. WiFi-Wardrive neighborhoods. This will expose your Geo Location if you are not using open proxies.

Use Exiv2 to remove metadata from some picture types:

```
exiv2 -d a *.png *.jpg
```

Use FFMPEG to remove some metadata from videos:

```
ffmpeg  -y -i my_input_file.mp4 -c copy -map_metadata -1 -metadata title="some file" -metadata creation_time=1997-01-01T01:01:00 -map_chapters -1 my_output_file.mp4
```

Tip: The output format must be the same as the input format. Convert to another format in a second pass.

Reset the timestamp on their files before adding to archive:

```
touch -t 199701010000 ./my_files/*
```

Do not let 7-zip add metadata to files: *hint: -mtm-*

```
7za a -t7z -m0=lzma2 -mx=9 -aoa -mfb=64 -md=32m -ms=on -mtm- ./file.7z ./dir/*
```

Or if you want to encrypt the files, also add:

```
-mhe=on -p
```

Don't use real names on their computer login.

# Run A Chan Or Blog Or Forum?

Maybe you can disable JavaScript for the people too lazy to block it themselves, at least for your own sites.

Add the following headers to your server:

```
x-dns-prefetch-control off
x-content-type-options nosniff
referrer-policy same-origin
content-security-policy "default-src 'self'; script-src 'none'; style-src 'self' 'unsafe-inline';"
```

- DNS Prefetch off stops some leakage from URL's people paste into your site, going into DNS servers outside of your domain.
- NoSniff stops the browser from guessing what a file really is. This blocks some malware pretending to be a picture.
- The same origin policy prevents referer leakage from your site into other site logs.
- The content security policy disables JavaScript for your site, but allows CSS and unsafe inline CSS, which most chans seem to require.

The method to add the header is slightly different in NGinx, Apache, HAProxy, so you will have to read up on how to add headers.

## Make .onion Tor Sites Faster?

**IF** you run both a .onion and Clearweb on the same site and you do not need to hide your server real IP address, then options you can set in your v3 .onion site torrc are

```
HiddenServiceSingleHopMode 0|1
HiddenServiceNonAnonymousMode 0|1
```

So if you set those to 1, know that you can not change them back. You will have to create a new .onion address, as that onion is forever not anonymous **for you, the server operator / admin**. End users browsing your site are still anonymous. This just removes 3 hops and makes your site faster.

You can also set HiddenServiceNumIntroductionPoints from 3 to as high as 20 on a v3 onion, to ensure your site is reachable, higher number risking more nodes know your HS IP address.

If you are running a chan site that is very fragile to individual users opening many connections, then consider the following v3 settings:

```
MaxOnionQueueDelay 2800
MaxClientCircuitsPending 1000
HiddenServiceMaxStreams 2000
HiddenServiceAllowUnknownPorts 0
```

Then set your KeepAlive time to somewhere between 3 and 9 seconds and enable defer-accept in your web server listener. HiddenServiceMaxStreams should be set just below whatever your web server can handle.

You can improve your web server capacity by forcing the caching of static content and pre-compressing static content. Confgure your server to drop client cache-control headers and ignore query strings. This breaks some RFC's but we have all fallen short of the glory of God.

## Why No HTTPS

LetsEncrypt does not yet support .onion sites.

For those curious, Tor server does use TLS, but one bug in the onion routing code and you are compromised.

Bugs are reported and fixed weekly. Not every bug will be reported. Not every reported bug will be fixed.

The Tor browser patches are always behind publicly available patches for Firefox ESR and this is a risk. Intermediate level developers can easily compare the changes to create exploit code.

HTTPS on Tor has positive and negative effects.

With HTTPS:

+ You get some additional privacy between you and the Tor site if Tor has a bug.
+ You can block MITM proxies if you pin the certs for websites into your browser.
- You can not filter content in Squid or Privoxy.
- You can not block dangerous protocols such as WebRTC, Websockets and DoH.
- You are exposing the version of SSL used by your client. This is a distinct fingerprint.

Without HTTPS or using SSL BUMP in Squid as Intercept Proxy:

+ You can filter out all HTTP headers that are not required to navigate a site.
+ You can filter out mime types that are dangerous.
+ You can reduce the risk of private data being leaked.
+ You can make all web clients look just like The Tor Browser.

## Latency: Why Is This Site Slow?

This TOR HS is just a proxy to a VPN mesh that uses a series of "borrowed" resources, thus not leaving any money trails.

The actual server is also a borrowed resource and is not my property.

This site can move to another borrowed resource automatically.

## PPH? *Posts Her Hour*

Site Usage Metrics are not available and not interesting.

## I Don't Like Something About This Site

This is not the site you are used to and it will never follow the same patterns of other chan sites, ever.

The style of this site changes all the time and is friendly to old cat ladies.

If this site really puts you off, then make the sites you like popular by visiting them instead of this one.

FWIW (For What Its Worth) The oldest version of this site is running inside of a mountain in China and broadcasting in the Khz range at 69 BAUD using a very simple cipher. That old version has been broadcasting well over 720 million years and survived several mass extinction events. LOL (Lucifer Our Lord)
