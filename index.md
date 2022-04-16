---
layout: default
title: Ju's Home!
---

# Ju's Home!

<div class="ju-pic" style="float: right; margin-left:10px;">
  <img src="https://avatars3.githubusercontent.com/u/28197089?s=460&v=4" width="200" height="200" alt="Ju drinking coffee">
</div>


My name is Ju Hang Sin, I'm a [programmer](https://github.com/juhangsin). I've been programming for the past 2 years. 1.5 years as a frontend developer, and 6 months as a backend API developer.


Currently, I work at a Toronto-based software development agency called [Bad Gateway](https://badgateway.net/) as a software developer. We specialize in building APIs and web applications for clients.

If you're interested in seeing my experience, here's my [Resume](/resume.html)

<ul>
  <li>Twitter : <a href="https://twitter.com/juhangsin" rel="me">@juhangsin</a></li>
  <li>Github : <a href="https://github.com/juhangsin" rel="me">juhangsin</a></li>
  <li><a href="/subscribe">Subscribe to my blog</a></li>
</ul>


## Archive

{% for post in site.posts %}
* {{ post.date | date:"%b %d" }} <a href="{{ post.url }}">{{ post.title }}</a>
{%endfor%}