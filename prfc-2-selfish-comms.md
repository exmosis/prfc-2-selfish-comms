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


***Internal Config***

****Firefox****

I use Firefox as it seems to offer the most consistent and complete cross-platform, cross-machine performance. That said, I have had problems running it on an underpowered Linux notebook where I've experimented with other browsers. (The [TorBrowser](https://www.torproject.org/projects/torbrowser.html) is often worth running when using Tor. [PaleMoon](http://www.palemoon.org/) and [Midori](http://midori-browser.org/) seem to be the most useful alternatives so far, at time of writing. However, keeping up with forks is time-consuming.)

*****Add-ons*****

The following add-ons have been chosen for being available equally on OSX and Android versions of Firefox, for consistency.

* *[HTTPS Everywhere](https://addons.mozilla.org/en-US/firefox/addon/https-everywhere/?src=search)* - encourage greater HTTPS usage for sites which support it. [HTTPS Everywhere homepage](https://www.eff.org/https-everywhere)
* *[uBlock Origin[(https://github.com/gorhill/uBlock)* - ad blocker.
* *[Decentraleyes](https://addons.mozilla.org/firefox/addon/decentraleyes)* offers a local version of various third-party files. See [simple description](https://github.com/Synzvato/decentraleyes/wiki/Simple-Introduction), still examining exactly what impact this has though.

OSX:

* Experimental: [Smart HTTPS](https://addons.mozilla.org/en-US/firefox/addon/smart-https/?src=search)

**Questions**


**Resources**



