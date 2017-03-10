---
ID: 231
post_title: >
  Setup XMPP with OMEMO encryption on your
  Desktop
author: Mathias Renner
post_date: 2016-12-07 21:38:19
post_excerpt: ""
layout: post
permalink: >
  https://bitleaf.de/2016/12/07/setup-xmpp-with-omemo-encryption-on-your-desktop/
published: true
---
In this article we will setup secure messaging on your desktop such that you have a safe wire to your friends – on all your devices.

<!--more-->

If you haven’t read “<a class="markup--anchor markup--p-anchor" href="https://medium.com/@mathiasrenner/setup-whatsapp-like-chat-messaging-with-open-source-software-complete-guide-ec7adc0d3519?source=user_profile---------2---------" target="_blank" data-href="https://medium.com/@mathiasrenner/setup-whatsapp-like-chat-messaging-with-open-source-software-complete-guide-ec7adc0d3519?source=user_profile---------2---------">Setup a Whatsapp-like chat messaging that respects your privacy–in just 10 minutes</a>”, read at least the introduction to understand why XMPP with OMEMO is useful. Best, take these 10 minutes and follow the instructions of the blog post.
<h3 id="6f59" class="graf graf--h3 graf-after--p"><strong>Requirements</strong></h3>
<ul class="postList">
 	<li id="4cdb" class="graf graf--li graf-after--h3"><strong class="markup--strong markup--li-strong">You need Ubuntu as Operating System on your Desktop</strong>
I show all steps using the operating system <strong class="markup--strong markup--li-strong">Ubuntu</strong>. With some effort, you can probably get it up and running <a class="markup--anchor markup--li-anchor" href="http://xmpp.org/software/clients.html" target="_blank" rel="nofollow noopener" data-href="http://xmpp.org/software/clients.html">on Windows and macOS</a>. However, a Linux operating system such as Ubuntu respects your privacy more, therefore I recommend using Linux.</li>
 	<li id="e8c8" class="graf graf--li graf-after--li"><strong class="markup--strong markup--li-strong">You do NOT need IT skills</strong></li>
</ul>
<h3 id="92a6" class="graf graf--h3 graf-after--li"><strong>Setup messenger on your Desktop</strong></h3>
<p id="b443" class="graf graf--p graf-after--h3">First, install all required software. To do so, open a terminal (use the search to open it or press <strong class="markup--strong markup--p-strong">STRG+ALT+t</strong>) and type:</p>

<pre id="3efc" class="graf graf--pre graf-after--p"><code class="markup--code markup--pre-code">sudo apt-get update &amp;&amp; sudo apt-get upgrade -y &amp;&amp; sudo apt-get install -y gajim python-appindicator python-axolotl</code></pre>
<p id="2258" class="graf graf--p graf-after--pre">Like this:</p>
<p class="graf graf--p graf-after--pre"><img class="aligncenter" src="https://cdn-images-1.medium.com/max/800/1*XATZotedIridfHpkPPTEdQ.png" /></p>
<p id="07f9" class="graf graf--p graf-after--figure">Then press enter. This installation will take some minutes. In the meantime, see the following list of what it installs or start with the next section.</p>

<ul class="postList">
 	<li id="c896" class="graf graf--li graf-after--p"><strong class="markup--strong markup--li-strong">Gajim</strong>: The Messenger we will use</li>
 	<li id="bde6" class="graf graf--li graf-after--li"><strong class="markup--strong markup--li-strong">Python-appindicator</strong>: It makes sure that you have an icon of Gajim in your menu bar of your Desktop, next to your system clock.</li>
 	<li id="6922" class="graf graf--li graf-after--li"><strong class="markup--strong markup--li-strong">Python-axolotl: </strong>Required to setup the security layer on top of XMPP</li>
</ul>
<p id="880e" class="graf graf--p graf-after--li">After the terminal finished its work, close it.</p>
<p id="06f2" class="graf graf--p graf-after--p">Next, start Gajim. You can use your Desktop search to do this. Gajim’s icon looks like this: <img class="aligncenter" src="https://cdn-images-1.medium.com/max/800/1*tTx1n36ptakX22HoviATQg.png" /></p>
<p class="graf graf--p graf-after--p">After Gajim has started, wait some seconds until it requests your permission to install updates:</p>
<p class="graf graf--p graf-after--p"><img class="aligncenter" src="https://cdn-images-1.medium.com/max/800/1*5xY0r-_6zzXCfgHb4NRa_w.png" /></p>
<p id="45d1" class="graf graf--p graf-after--figure">Allow this. Afterwards, a new window will open that lists all components that can be updated. In this list, activate the checkbox next to <strong class="markup--strong markup--p-strong">Appindicator Integration </strong>and <strong class="markup--strong markup--p-strong">OMEMO</strong>. Then, click on the button I<strong class="markup--strong markup--p-strong">nstall/Upgrade</strong> on the bottom left on that window.</p>
<p id="b0e1" class="graf graf--p graf-after--p">After the update has finished, go to the other tab <strong class="markup--strong markup--p-strong">Installed</strong>. There, make sure that all components are activated via the checkbox. Afterwards, click <strong class="markup--strong markup--p-strong">close </strong>on the bottom right of the window.</p>
<p id="0ebd" class="graf graf--p graf-after--p">Then, you should see a wizard to setup your XMPP account. Select the option that you already have an account and follow all instructions yourself using the default settings.</p>
<p class="graf graf--p graf-after--p"><img class="aligncenter" src="https://cdn-images-1.medium.com/max/800/1*dgFS20eryuNyhYmPdcPkpg.png" /></p>
<p id="60d5" class="graf graf--p graf-after--figure">After you finished the wizard successfully, Gajim will show your status as <strong class="markup--strong markup--p-strong">Available</strong>. Congratulations! Now, let’s send messages to your friends.</p>
<p id="e198" class="graf graf--p graf-after--p">To do so, click on the Gajim window and move your mouse to the top of the screen. There, a menu should appear. Go to <strong class="markup--strong markup--p-strong">Actions</strong> -&gt; <strong class="markup--strong markup--p-strong">Start chat… </strong>. In the new window, add the XMPP ID of your friend and click <strong class="markup--strong markup--p-strong">ok</strong>.</p>
<p class="graf graf--p graf-after--p"><img class="aligncenter" src="https://cdn-images-1.medium.com/max/800/1*J_CI-jdZCHYqVASFasYKhw.png" /></p>
<p id="4ec2" class="graf graf--p graf-after--figure">A chat windows opens up. Just close this window. Go to the main menu again and select <strong class="markup--strong markup--p-strong">View</strong> -&gt; <strong class="markup--strong markup--p-strong">Show offline contacts…</strong> .</p>
<p id="76b6" class="graf graf--p graf-after--p">In the Gajim window, you should see your friend. Right click on the name of your friend and select <strong class="markup--strong markup--p-strong">Manage contact</strong> -&gt; <strong class="markup--strong markup--p-strong">Add to roster</strong>. In the pop up, just click <strong class="markup--strong markup--p-strong">Add</strong>. Now your friend is permanently added to your list of contacts.</p>
<p id="34b0" class="graf graf--p graf-after--p">Next, right click on your friend and select <strong class="markup--strong markup--p-strong">Manage contact</strong> -&gt; <strong class="markup--strong markup--p-strong">Allow subscription</strong> -&gt; <strong class="markup--strong markup--p-strong">Allow contact to see my status</strong>.</p>
<p id="a945" class="graf graf--p graf-after--p">Your friend should see a request like this:</p>
<p class="graf graf--p graf-after--p"><img class="aligncenter" src="https://cdn-images-1.medium.com/max/800/1*8HOTjPsgjapZxJNjrWcKpQ.png" /></p>
<p class="graf graf--p graf-after--p">He shall click <strong class="markup--strong markup--p-strong">Authorize</strong>, which enables him to see if you are online or not. Also, this step is necessary for activating the encryption.</p>
<p class="graf graf--p graf-after--p">Next, make sure that your friend also allows you to see his status.</p>
<p class="graf graf--p graf-after--p"><strong class="markup--strong markup--p-strong"><em class="markup--em markup--p-em">Note: At any point in time from now on, you will be asked to trust something called “fingerprints”. In this case, jump to the section “All about fingerprints” one block further down.</em></strong></p>
<p class="graf graf--p graf-after--p">Now, when you open the chat window to your friend, it should say <strong class="markup--strong markup--p-strong">OMEMO encryption enabled</strong> and show a red shield next to the input field, like this:</p>
<p class="graf graf--p graf-after--p"><img class="aligncenter" src="https://cdn-images-1.medium.com/max/800/1*iVS618vri0a1byRrXMm2nA.png" /></p>
<p id="e3b7" class="graf graf--p graf-after--figure">If you don’t see the <strong class="markup--strong markup--p-strong">OMEMO encryption enabled </strong>— just restart Gajim and have a look again.</p>
<p id="be6c" class="graf graf--p graf-after--p"><strong class="markup--strong markup--p-strong">Congratulations! That’s all!</strong></p>
<p id="d3da" class="graf graf--p graf-after--p"><strong class="markup--strong markup--p-strong">If you wanna chat also on your Smartphone,</strong><a class="markup--anchor markup--p-anchor" href="https://medium.com/@mathiasrenner/setup-whatsapp-like-chat-messaging-with-open-source-software-complete-guide-ec7adc0d3519#.9xbv7f2zd" target="_blank" data-href="https://medium.com/@mathiasrenner/setup-whatsapp-like-chat-messaging-with-open-source-software-complete-guide-ec7adc0d3519#.9xbv7f2zd"><strong class="markup--strong markup--p-strong"> just follow this </strong></a><a class="markup--anchor markup--p-anchor" href="http://guide/" target="_blank" rel="nofollow noopener" data-href="http://guide"><strong class="markup--strong markup--p-strong">guide</strong></a><strong class="markup--strong markup--p-strong">.</strong></p>

<h3 id="904c" class="graf graf--h4 graf-after--p"><strong>All about “Fingerprints”</strong></h3>
<p id="b088" class="graf graf--p graf-after--h4"><strong class="markup--strong markup--p-strong"><em class="markup--em markup--p-em">Note:</em></strong><em class="markup--em markup--p-em"> Read this subsection only when you are asked to trust something called “fingerprints”. Otherwise, just skip it!</em></p>
<p id="9145" class="graf graf--p graf-after--p">Simply put, a fingerprint is an ID of a devices someone uses for the messaging. In order to make sure that you communicate with exact the devices, which your friend uses, you need to see if the fingerprints listed in this window match with the ones your friend really has.</p>
<p id="fbf8" class="graf graf--p graf-after--p">So, ask your friend to list his fingerprints on his desktop. On his computer, in the chat window with you, he shall click on the setting symbol below the text input field (grey, with wheels). There he goes to <strong class="markup--strong markup--p-strong">OMEMO encryption</strong>  -&gt; <strong class="markup--strong markup--p-strong">Fingerprints</strong>. He should now see the same window as you.</p>
<p id="2bb8" class="graf graf--p graf-after--p">He should chose the tab <strong class="markup--strong markup--p-strong">Own devices</strong>, while you chose the tab <strong class="markup--strong markup--p-strong">Contact</strong>. Now, select a fingerprint that matches with the one of your friend and press the button <strong class="markup--strong markup--p-strong">Trust/Revoke Fingerprint</strong>. Also press <strong class="markup--strong markup--p-strong">yes</strong> in the window that appears.</p>
<p id="dc03" class="graf graf--p graf-after--p">Finally, all fingerprints should be green like this:</p>
<img class="aligncenter" src="https://cdn-images-1.medium.com/max/800/1*PHD5IIBH-Vlgz5u9Wdm1uQ.png" />

That’s all about fingerprints! Now, please move on at exactly the instructions before you jumped to this fingerprint section.
<h3 id="dbf0" class="graf graf--h3 graf-after--p"><strong>Known Bugs</strong></h3>
<ul class="postList">
 	<li id="566d" class="graf graf--li graf-after--h3">In the main menu of Gajim, not all options work. Luckily, the important ones do.</li>
 	<li id="8c12" class="graf graf--li graf-after--li">Gajim is not able to send a confirmation if you’ve read a message. Conversations can.</li>
 	<li id="f0dc" class="graf graf--li graf-after--li">Gajim sometimes reports that your friend did not get the message even if he did.</li>
</ul>
<h3 id="6862" class="graf graf--h3 graf-after--li"><strong>Troubleshooting</strong></h3>
<ul class="postList">
 	<li id="6466" class="graf graf--li graf-after--h3">Sometimes, a restart of Gajim just helps :)</li>
 	<li id="2ebd" class="graf graf--li graf-after--li">If OMEMO encryption or the fingerprint option is grey and cannot be activated, just send a message in the chat window. This sometimes helps.</li>
</ul>
<p id="c4a0" class="graf graf--p graf-after--li graf--trailing">Please report issues in the comments below.</p>
This article has also been published <a href="https://medium.com/@mathiasrenner/setup-xmpp-with-omemo-encryption-on-your-desktop-7f6accd8dc16#.e7lmq5dm5">on my private blog</a>.