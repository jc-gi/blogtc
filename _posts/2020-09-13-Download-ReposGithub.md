---
layout: post
section-type: post
title: Install Brew and download repositories of github account
category: tech
tags: [ 'tutorial' ]
---
Alternative Installation
Extract or git clone Homebrew wherever you want. Use /home/linuxbrew/.linuxbrew if possible (to enable the use of binary packages).

git clone https://github.com/Homebrew/brew ~/.linuxbrew/Homebrew
mkdir ~/.linuxbrew/bin
ln -s ~/.linuxbrew/Homebrew/bin/brew ~/.linuxbrew/bin
eval $(~/.linuxbrew/bin/brew shellenv)

<pre><code data-trim class="yaml">
Download repos of github account
curl -s https://api.github.com/users/jc-gi/repos | grep \"clone_url\" | awk '{print $2}' | sed -e 's/"//g' -e 's/,//g' | xargs -n1 git clone

curl -s https://api.github.com/users/upslp-teoriacomputacional/repos | grep \"clone_url\" | awk '{print $2}' | sed -e 's/"//g' -e 's/,//g' | xargs -n1 git clone



<small>Many thanks to <a href="https://github.com/jc-gi" target="\_blank">@jc-gi</a> for this feature!</small>
