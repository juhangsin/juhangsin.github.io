---
layout: default
title: Ju's Home!
---

# Ju's Home!

<div class="ju-pic">
  <img src="https://avatars3.githubusercontent.com/u/28197089?s=460&v=4" width="200" height="200" alt="Ju drinking coffee">
</div>


My name is Ju-Hang Sin, I'm a [programmer](https://github.com/juhangsin). I've been programming for the past 2 years. 1.5 years as a frontend developer, and 6 months as a backend API developer.


Currently, I work at a Toronto-based software development agency [Bad Gaetway](https://badgateway.net/) as a software developer. We specializes in building APIs and web applications for clients.

If you're interested in seeing my expierence, here's my [Resume](/resume.html)

## Archive

{% for post in site.posts %}
* {{ post.date | date:"%b %d" }} <a href="{{ post.url }}">{{ post.title }}</a>
{%endfor%}