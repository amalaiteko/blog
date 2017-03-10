---
ID: 516
post_title: Encrypting with GPG is fun!
author: Mathias Renner
post_date: 2015-11-17 23:10:49
post_excerpt: ""
layout: post
permalink: >
  https://bitleaf.de/2015/11/17/encrypting-with-gpg-is-fun/
published: true
wpgs_notice_id:
  - "9176081"
wpgs_conversation_id:
  - "8247885"
wpgs_updating:
  - "0"
wpgs_laste_komentis:
  - 2017-02-16 22:10:51
---
<p class="graf graf--h4 graf-after--figure">Why do you not encrypt? Because it is not fun, right? I'll show you how much fun it can be :-)</p>

<!--more-->

<p id="db7f" class="graf graf--p graf-after--h4">Encryption often is not fun at first sight. Either you go for an open source tool, but the user experience suffers by non-intuitive interfaces. Or you choose a proprietary tool, which does ship a neat interface, but you can never be sure whether you also bought a backdoor.</p>

<p id="310f" class="graf graf--p graf-after--p">In addition, you want a tool that is commonly adopted such that the friend receiving your encrypted data does not need to install a tool just to decrypt your data.</p>

<p id="86ed" class="graf graf--p graf-after--p">Also, if you want to sync your encrypted data somewhere, a large <a class="markup--anchor markup--p-anchor" href="https://veracrypt.codeplex.com/" target="_blank" rel="nofollow noopener" data-href="https://veracrypt.codeplex.com/">Truecrypt/Veracrypt</a> container is not justified to be synchronized after just one of its containing files has been changed.</p>

<h3 id="aed6" class="graf graf--h4 graf-after--p"><strong>Give GPG a chance and enjoy it</strong></h3>

<p id="7c6b" class="graf graf--p graf-after--h4">I think that encryption can be lots of fun as long as you use the appropriate tools. One of my most loved ones is <strong class="markup--strong markup--p-strong">GNU P</strong>rivacy <strong class="markup--strong markup--p-strong">G</strong>uard<em class="markup--em markup--p-em"> (</em>GPG), which meets the challenges stated above quite well: It is open source, actively developed since 1997 and thus very stable, installed on many Linux distributions by default, and encrypts file by file, which results in high sync performance. Also, it is super easy to use once it is properly set-up.</p>

<p id="5166" class="graf graf--p graf-after--p"><a class="markup--anchor markup--p-anchor" href="https://www.digitalocean.com/community/tutorials/how-to-use-gpg-to-encrypt-and-sign-messages-on-an-ubuntu-12-04-vps" target="_blank" rel="nofollow noopener" data-href="https://www.digitalocean.com/community/tutorials/how-to-use-gpg-to-encrypt-and-sign-messages-on-an-ubuntu-12-04-vps">This is an awesome article</a> that covers everything from setup to usage of GPG. If you have been convinced by the end of this post that GPG is something you want to get your hands on, follow this article. In the following, I will only show how easy it is to use GPG after its one-time setup.</p>

<h3 id="7a29" class="graf graf--h4 graf-after--p"><strong class="markup--strong markup--h4-strong">Option 1: Symmetric encryption (simple)</strong></h3>

<p id="7846" class="graf graf--p graf-after--h4">You encrypt with</p>

<pre id="d568" class="graf graf--pre graf-after--p">gpg -c file_name</pre>

<p id="0646" class="graf graf--p graf-after--pre">and provide a password. The receiver decrypts with</p>

<pre id="c266" class="graf graf--pre graf-after--p">gpg file_name</pre>

<p id="4b27" class="graf graf--p graf-after--pre">and is asked to type the same password. That’s all.</p>

<h3 id="b683" class="graf graf--h4 graf-after--p"><strong class="markup--strong markup--h4-strong">Option 2: Asymmetric encryption (more secure)</strong></h3>

<p id="e382" class="graf graf--p graf-after--h4">You encrypt by providing your and the receiver’s email address:</p>

<pre id="bf11" class="graf graf--pre graf-after--p">gpg -r you@you.com -r recipient@recipient.com --encrypt file_name</pre>

<p id="ef91" class="graf graf--p graf-after--pre">The receiver decrypts by just typing</p>

<pre id="badf" class="graf graf--pre graf-after--p">gpg file_name</pre>

<p id="8003" class="graf graf--p graf-after--pre">Finished.</p>

<p id="2650" class="graf graf--p graf-after--p">You can also encrypt multiple files in (sub)folders with</p>

<pre id="5d67" class="graf graf--pre graf-after--p">gpg -r you@you.com -r recipient@recipient.com --encrypt-files $(find -type f)</pre>

<h3 class="graf graf--h4 graf-after--pre"><strong>
GUIs decrypt automatically!</strong></h3>

<p id="bad7" class="graf graf--p graf-after--h4">Using available <strong class="markup--strong markup--p-strong">g</strong>raphical <strong class="markup--strong markup--p-strong">u</strong>ser <strong class="markup--strong markup--p-strong">i</strong>nterfaces (GUIs), a double click on the encrypted file will automatically decrypt it! Of course, this holds only for option 2 (asymmetric). If the file has been encrypted with a password, after the double click you will be prompted to provide the password. Not much more difficult either…</p>

<p id="cb18" class="graf graf--p graf-after--p">For instance, a GUI are available in <strong class="markup--strong markup--p-strong">Ubuntu.</strong> You will be prompted to install missing packages after you clicked on an encrypted file at the first time. Otherwise, install seahorse-daemon, seahorse-nautilus and libcryptui0a manually. For <strong class="markup--strong markup--p-strong">Mac</strong> install <a class="markup--anchor markup--p-anchor" href="https://gpgtools.org/" target="_blank" rel="nofollow noopener" data-href="https://gpgtools.org/">GPG tools</a>, which include everything you need out-of-the box.</p>

<p id="9109" class="graf graf--p graf-after--p graf--trailing">It is too easy to not to get started. Happy crypto party!</p>

<p class="graf graf--p graf-after--p graf--trailing">This article has also been published <a href="https://medium.com/@mathiasrenner/encrypting-with-gpg-is-fun-d68f48a105cb#.q1zyfzxpp">on my private blog</a>.</p>

<footer class="u-paddingTop10">
<div class="container u-maxWidth740"></div>
</footer>