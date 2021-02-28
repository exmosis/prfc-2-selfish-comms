**Summary**

This [PRFC](https://github.com/exmosis/prfc-0-prfcs/blob/master/prfc-0.md) sets out a description/plan for establishing more secure communications across my personal devices, computers, servers, etc. It aims to list the services and settings being used, or which could be used, as well as any particular reasons or known omissions. 

Hopefully this may be of use to others?

**Meta**

Authors: @[6loss](https://twitter.com/6loss)<br>
Version: Draft v0.1.0<br>
URL: https://github.com/exmosis/prfc-2-selfish-comms<br>

**Background**

I started using the internet in around 1995. At this time, personal data was fairly lacklustre on the internet, and there were very few on-line connections that mirrored off-line ones - "cyberspace" was more a place for meeting other identities, not for continuing interaction with lost friends and remote family. As such, on the whole there was a sense of "mistrust" - or rather, strangers needed to prove their trust before personally-identifying information was handed over. Real names, addresses, telephone numbers were not a necessity, and not to be handed out to all and sundry.

Over the next 20 years, the internet transformed into a megamachine of convenience, and this convenience brought with it a certain amount of both naivety (on the part of users) and opportunity (on the part of venture capitalists) - this valuable information, closely guarded before, started to be teased out in various ways, so that its value could be turned into *economic* value. The Foucauldian notion of the individual's data and metadata as a control mechanism was finally given a fully-fledged, automated, global network representation in which personal data was the new gold. Furthermore, the networked nature of this newly-wrought communication model meant that *inter*personal data - the combination of individuas, who was talking to who, etc - could be captured fully and fastidiously for the first time.

This PRFC does not assume tht this set-up must *inherently* lead to a conclusion that those who monitor the network are evil, corrupt or controlling. But from a single user's point of view, there is no way to know a) what data and metadata is truly being captured (only what is *legally* set out), b) which entities are using such data, and c) what they are using it for.

It is this lack of knowing that this PRFC seeks to address, not the lack of trust, and we address this by attempting to mask and "selfishly own" as much of our own data as possible. This primarily includes forms of encryption, but also extends out to other techniques such as obfuscation, chaff, and continuous data obsolesence.

**Aims**

1. Disrupt any external parties' ability to gain a single, complete picture of the activity and intent of a particular user.

**Spec**

This section will be broken down by external services and internal setup.

***External Services***

****Virtual Private Network****

A Virtual Private Network (VPN) can be useful for a number of purposes. It can provide a secure, (more) trusted link when on an otherwise insecure connection (such as a cafe wifi), and can also encrypt traffic in order to bypass other interception (such as ISPs that knowingly intercept or block certain types of traffic, such as webpages.

As of December 2016, I use [Trust.Zone](https://trust.zone/)  - it should be noted this is my first use of a personal VPN, and still subject to experiment, but initial results are encouraging. You may also be interested in this [heady introduction and guide to what to look for in a VPN](https://www.reddit.com/r/VPN/comments/4iho8e/that_one_privacy_guys_guide_to_choosing_the_best/?st=iu9u47u7&sh=459a76f2). Trust.Zone has several servers based around the world and it's easy to jump country by changing the server being connected to. You can also pay in Bitcoin, and they allow traffic such as Tor connections. They claim not to log anything (although I haven't done more work fully verifying this yet) and have good setup guides to follow. So far, support is good for OSX and Android devices (see below for internal configuration).

***Internal Config***

****VPN setup****

See above for more info on the Trust.Zone, the VPN service I'm currently using. For all clients below, I tend to connect to a VPN server in *Switzerland* as a primary option, and *Brazil* as a secondary option. I've started looking into the [14 Eyes countries](https://www.my-private-network.co.uk/vpn-provider-14-eyes-country-something-know/) which is worth reading up on if looking to find out how information is gathered internationally.

*****OSX*****

Trust.Zone support OpenVPN and L2TP for OSX - I use L2TP over IPSec, configured using OSX's own internal VPN setup. 

*****Android*****

I use the [OpenVPN for Android](https://ics-openvpn.blinkt.de) app for Android, which is available via [F-Droid](http://f-droid.org/). The configuration file for this can be downloaded from the Trust.Zone site, and should work easily once you enter your connection's username and password.

I make sure OpenVPN is ocnfigured to disallow network traffic when the VPN is reconnecting.

*Known issue:* There is a small amount of time on boot-up when the wi-fi network is enabled, but OpenVPN is still connecting. Some known background apps may try to connect without the VPN at this point. Currently this is a known potential leak, but an acceptable risk so far. Possible workarounds include 1) turning off auto-sync (or running in Battery Saver mode?) and 2) rooting the device to have more control over traffic (although this has other risks).

****Firefox****

I use Firefox as it seems to offer the most consistent and complete cross-platform, cross-machine performance. That said, I have had problems running it on an underpowered Linux notebook where I've experimented with other browsers. (The [TorBrowser](https://www.torproject.org/projects/torbrowser.html) is often worth running when using Tor. [PaleMoon](http://www.palemoon.org/) and [Midori](http://midori-browser.org/) seem to be the most useful alternatives so far, at time of writing. However, keeping up with forks is time-consuming.)

*****Add-ons*****

The following add-ons have been chosen for being available equally on OSX and Android versions of Firefox, for consistency.

* *[HTTPS Everywhere](https://addons.mozilla.org/en-US/firefox/addon/https-everywhere/?src=search)* - encourage greater HTTPS usage for sites which support it. [HTTPS Everywhere homepage](https://www.eff.org/https-everywhere)
* *[uBlock Origin](https://github.com/gorhill/uBlock)* - ad blocker. [NoScript](https://noscript.net/) is a more stringent alternative, but breaks more sites.
* *[Decentraleyes](https://addons.mozilla.org/firefox/addon/decentraleyes)* offers a local version of various third-party files. See [simple description](https://github.com/Synzvato/decentraleyes/wiki/Simple-Introduction), still examining exactly what impact this has though.
* *[ProxyBonanza Proxy Manager](https://addons.mozilla.org/en-US/firefox/addon/proxybonanza-manager/?src=ss)* - for proxy setup/switching
* *[Disconnect for Facebook](https://mybrowseraddon.com/facebook-disconnect.html)* - for avoiding Facebook

Under test:

* *[Privacy Badger](https://www.eff.org/privacybadger)* - the EFF's version of a blocker, based on analysing site traffic as you browse
* *[NeatURL](https://addons.mozilla.org/en-US/firefox/addon/neat-url/?src=search)* - one of various add-ons to remove tracking parameters in URLs
 * Possible alternative is [ClearURLs](https://addons.mozilla.org/en-US/firefox/addon/clearurls/), but this requires a lot more permissions granted
 
OSX:

* Experimental: [Smart HTTPS](https://addons.mozilla.org/en-US/firefox/addon/smart-https/?src=search)

**Questions**


**Resources**

* Useful guide which covers much of the same: https://www.privacytools.io/#addons
* A [ghacks guide](https://github.com/ghacksuserjs/ghacks-user.js/wiki/4.1-Extensions) worth looking at
* Whoa: [Humane Tech's guide](https://github.com/humanetech-community/awesome-humane-tech) looks amazing
* Bruce Schneier: [Should there be limits on persuasive technologies?](https://www.schneier.com/blog/archives/2020/12/should-there-be-limits-on-persuasive-technologies.html)
* 



