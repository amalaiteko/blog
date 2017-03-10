---
ID: 226
post_title: >
  Setup a Whatsapp-like chat messaging
  that respects your privacy–in just 10
  minutes
author: Mathias Renner
post_date: 2016-11-28 21:33:11
post_excerpt: ""
layout: post
permalink: >
  https://bitleaf.de/2016/11/28/setup-a-whatsapp-like-chat-messaging-that-respects-your-privacy-in-just-10-minutes/
published: true
---
<span class="graf-dropCap">T</span>his guide helps using a chat messenger on your phone that works like Whatsapp or Facebook Messenger, but which respects your privacy and freedom.<!--more-->

This alternative is:

<ul class="postList">
    <li id="2410" class="graf graf--li graf-after--p"><strong class="markup--strong markup--li-strong">Open source</strong> — the technology is open, available for everyone to check if it’s secure or not</li>
    <li id="3669" class="graf graf--li graf-after--li"><strong class="markup--strong markup--li-strong">Decentralized</strong> — servers are not all controlled by a single company, but run by volunteers, organizations and many companies that value privacy</li>
    <li id="c625" class="graf graf--li graf-after--li"><strong class="markup--strong markup--li-strong">Highly secure</strong> — the underlying technology has been <a class="markup--anchor markup--li-anchor" href="http://www.theverge.com/2015/11/3/9662724/signal-encrypted-chat-app-android-edward-snowden" target="_blank" rel="nofollow noopener" data-href="http://www.theverge.com/2015/11/3/9662724/signal-encrypted-chat-app-android-edward-snowden">recommended by Edward Snowden</a>, an independent <a class="markup--anchor markup--li-anchor" href="https://conversations.im/omemo/audit.pdf" target="_blank" rel="nofollow noopener" data-href="https://conversations.im/omemo/audit.pdf">security audit</a> has been performed, and <a class="markup--anchor markup--li-anchor" href="https://conversations.im/omemo/" target="_blank" rel="nofollow noopener" data-href="https://conversations.im/omemo/">important security features</a> like <em class="markup--em markup--li-em">end-to-end encryption</em> and <em class="markup--em markup--li-em">Perfect Forward Secrecy</em> are included.</li>
</ul>

<p id="bf4a" class="graf graf--p graf-after--li"><strong class="markup--strong markup--p-strong">The software we’ll use (called “XMPP” and “OMEMO”) is now a powerful and secure messaging technology for the masses</strong>. I’ve followed its development for several years now. Just recently, both the feature set and the usability of this technology has improved so much that it’s not any more for IT geeks only. After setup, it works as easy as Whatsapp.</p>

<strong class="markup--strong markup--p-strong">I highly recommend to follow this guide with a friend who also wants to use this technology.</strong> Then you can help each other out and immediately test if everything works.

<p id="7e92" class="graf graf--p graf-after--p">You wanna know more about this technology and why it is useful? <a class="markup--anchor markup--p-anchor" href="https://www.kuketz-blog.de/conversations-sicherer-android-messenger/" target="_blank" rel="nofollow noopener" data-href="https://www.kuketz-blog.de/conversations-sicherer-android-messenger/">This blog post</a> is a wonderful introduction. Unfortunately, it’s only available in German. However, some more research should yield in good English content as well. Just look for “XMPP” and “OMEMO”.</p>

<h3 id="6f59" class="graf graf--h3 graf-after--p"><strong class="markup--strong markup--h3-strong">The Requirement</strong></h3>

<p id="13f8" class="graf graf--p graf-after--h3"><strong class="markup--strong markup--p-strong">Only Android as Operating System on your Smartphone. </strong><a class="markup--anchor markup--p-anchor" href="http://xmpp.org/software/clients.html" target="_blank" rel="nofollow noopener" data-href="http://xmpp.org/software/clients.html">There are apps for iOS and others</a>, but we’ll use Android. In best case, you rooted your Android phone and don’t have Google Apps installed on it.</p>

<h3 id="a137" class="graf graf--h3 graf-after--p"><strong>1. Download the messenger app on your Smartphone</strong></h3>

<p id="5552" class="graf graf--p graf-after--h3"><strong class="markup--strong markup--p-strong">If you want it for free, </strong>you need to install the alternative app store <strong class="markup--strong markup--p-strong">f-droid </strong>before. F-droid works like Google Play, but only offers apps that are free and based on open source. See instructions in the next paragraph how to install f-droid.
<strong class="markup--strong markup--p-strong">If you wanna use Google’s play store</strong>, it’s between $2 and $3. Open Google Play and download the app <strong class="markup--strong markup--p-strong">Conversations.</strong></p>

<p id="35c0" class="graf graf--p graf-after--p">If you decided for f-droid, open the website <a class="markup--anchor markup--p-anchor" href="https://f-droid.org/" target="_blank" rel="nofollow noopener" data-href="https://f-droid.org/">https://f-droid.org/</a> with the browser on your phone. Press the big download button on the website, which will download f-droid’s installer. After download, press the downloaded file and the installer should start. Next, start f-droid and search for the apps <strong class="markup--strong markup--p-strong">Conversations</strong>. Conversations is the messenger we will use. Install it.</p>

<h3 id="c77c" class="graf graf--h3 graf-after--p"><strong>2. Start the messenger app and register</strong></h3>

<p id="6e2c" class="graf graf--p graf-after--h3">Now, start <strong class="markup--strong markup--p-strong">Conversations</strong>. In the app, add an account.</p>

<p id="4cf3" class="graf graf--p graf-after--p">If you already have an account (= Jabber ID or XMPP ID), provide your credentials. If you do not have an account yet, I recommend you register on the server <strong class="markup--strong markup--p-strong">talker.to. </strong>You can register at any server available (<a class="markup--anchor markup--p-anchor" href="https://gultsch.de/compliance_ranked.html" target="_blank" rel="nofollow noopener" data-href="https://gultsch.de/compliance_ranked.html">server list 1</a>, <a class="markup--anchor markup--p-anchor" href="https://xmpp.net/directory.php" target="_blank" rel="nofollow noopener" data-href="https://xmpp.net/directory.php">list 2</a>), but I recommend that one because compared to other XMPP servers it has <a class="markup--anchor markup--p-anchor" href="https://xmpp.net/result.php?domain=talker.to&amp;type=server" target="_blank" rel="nofollow noopener" data-href="https://xmpp.net/result.php?domain=talker.to&amp;type=server">very high security specifications,</a> it’s <a class="markup--anchor markup--p-anchor" href="https://www.iplocation.net/" target="_blank" rel="nofollow noopener" data-href="https://www.iplocation.net/">located in Germany</a> and it offers <a class="markup--anchor markup--p-anchor" href="https://gultsch.de/compliance_ranked.html" target="_blank" rel="nofollow noopener" data-href="https://gultsch.de/compliance_ranked.html">many features</a> (like sending files in chats etc.).</p>

<p id="a2c4" class="graf graf--p graf-after--p">If you wanna register a new account, also active the checkbox. Finally, it should look like this:</p>

&nbsp;

<img class="aligncenter" src="https://cdn-images-1.medium.com/max/800/1*997ziudt9Qz3znfq2u68YQ.png" />

After you clicked <strong class="markup--strong markup--p-strong">Next</strong>, the registration process might take up to 20 seconds. If everything was successful, you see this:

<img class="aligncenter" src="https://cdn-images-1.medium.com/max/800/1*Lb6dRMFXdwf3FnF96RivQw.png" />

For now, just press <strong class="markup--strong markup--p-strong">skip.</strong>

<h3 id="c9d7" class="graf graf--h3 graf-after--p"><strong>3. Start chatting</strong></h3>

<p id="de0b" class="graf graf--p graf-after--h3">Congrats, you now you have an account for yourself. Let’s use it and start a conversation with a friend. Click on the plus on the top right to add a conversation</p>

<p class="graf graf--p graf-after--h3"><img class="aligncenter" src="https://cdn-images-1.medium.com/max/800/1*MOnO1RMTIdq0ZCdAkDfOOA.png" /></p>

If your list of contacts is empty, add a new contact:

<img class="aligncenter" src="https://cdn-images-1.medium.com/max/800/1*JMUihL4mDqd97E5hs1geFw.png" />

<p id="724f" class="graf graf--p graf-after--figure">Insert your friend’s Jabber ID, e.g. <strong class="markup--strong markup--p-strong">your-friend@a-jabber-server.com</strong></p>

<p id="eb87" class="graf graf--p graf-after--p">That’s it. You can now chat with your friend. However, this will be unencrypted! So let’s activate OMEMO encryption by pressing the padlock in the top menu bar:</p>

<img class="aligncenter" src="https://cdn-images-1.medium.com/max/800/1*CPgE-78jMO2NsELgbH6Hww.png" />

<p id="0a63" class="graf graf--p graf-after--figure">After you activated OMEMO, the input field at the bottom should say you can now send encrypted messages:</p>

<div class="aspectRatioPlaceholder is-locked"><img class="aligncenter" src="https://cdn-images-1.medium.com/max/800/1*CMBT5V0TS9w9cr0Dlct_cQ.png" /></div>

<div class="aspectRatioPlaceholder is-locked"></div>

<div class="aspectRatioPlaceholder is-locked">
<p id="efab" class="graf graf--p graf-after--figure"><strong class="markup--strong markup--p-strong">Congratulations, that’s all! </strong>Who thought that setting up the best available messaging tool is as easy as that? (To me, “best” means decentralized, open source, secure and good usability, of course.)</p>
<p id="739d" class="graf graf--p graf-after--p"><strong class="markup--strong markup--p-strong">If you wanna chat also on your Desktop, </strong><a class="markup--anchor markup--p-anchor" href="https://medium.com/@mathiasrenner/setup-xmpp-with-omemo-encryption-on-your-desktop-7f6accd8dc16#.oitm88cyj" target="_blank" data-href="https://medium.com/@mathiasrenner/setup-xmpp-with-omemo-encryption-on-your-desktop-7f6accd8dc16#.oitm88cyj"><strong class="markup--strong markup--p-strong">just follow this guide.</strong></a></p>

<h3 id="e77c" class="graf graf--h3 graf-after--p"><strong>Troubleshooting</strong></h3>
<ul class="postList">
    <li id="2ebd" class="graf graf--li graf-after--h3"><strong class="markup--strong markup--li-strong">If OMEMO cannot be activated</strong>, just send a message in the chat window. This sometimes helps. Also, it may help to end a conversation by pressing the menu on the top right inside a conversation as shown in the following screenshot, and then re-open the conversation again.</li>
</ul>
</div>

<div class="aspectRatioPlaceholder is-locked"><img class="aligncenter" src="https://cdn-images-1.medium.com/max/800/1*FpFt-XXZ-tCaRGr7aS1c4w.png" /></div>

<div class="aspectRatioPlaceholder is-locked"></div>

<div class="aspectRatioPlaceholder is-locked">
<ul class="postList">
    <li id="7cea" class="graf graf--li graf-after--figure"><strong class="markup--strong markup--li-strong">Allow presence updates:</strong> In a conversation, click on the icon/image of your chat partner. In the new screen (as shown below), make sure that all check boxes are activated:</li>
</ul>
</div>

<div class="aspectRatioPlaceholder is-locked"><img class="aligncenter" src="https://cdn-images-1.medium.com/max/800/1*ku0_nR9JeEGi4RxKU1ESqw.png" /></div>

<div class="aspectRatioPlaceholder is-locked"></div>

<div class="aspectRatioPlaceholder is-locked">
<ul class="postList">
    <li id="c859" class="graf graf--li graf-after--figure"><strong class="markup--strong markup--li-strong">Check fingerprints: </strong>You might be asked to trust fingerprints like this:</li>
</ul>
</div>

<div class="aspectRatioPlaceholder is-locked"><img class="aligncenter" src="https://cdn-images-1.medium.com/max/800/1*r-Y1xRgVSg8bUJepk5FCuw.png" /></div>

<div class="aspectRatioPlaceholder is-locked"></div>

<div class="aspectRatioPlaceholder is-locked">
<p id="664d" class="graf graf--p graf-after--figure">OMEMO only works fine, if the fingerprint of your and your friend’s device match. To compare them, open one of your conversations and click on your icon next to one of your messages. At the same time, your friend clicks on <strong class="markup--strong markup--p-strong">your</strong> icon on his phone. Now, both of you should see a fingerprint that you can check. If they match, change the slider as you see in the screenshot to the right.</p>
<p id="7023" class="graf graf--p graf-after--p graf--trailing"><em class="markup--em markup--p-em">If you still have issues after trying out all troubleshooting tips, please report your case in the comments below.</em></p>

</div>

<div class="aspectRatioPlaceholder is-locked"></div>

This article has also been published <a href="https://medium.com/@mathiasrenner/setup-whatsapp-like-chat-messaging-with-open-source-software-complete-guide-ec7adc0d3519#.hgltf5h50">on my private blog</a>.