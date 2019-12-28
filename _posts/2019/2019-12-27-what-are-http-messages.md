---
title: "What Are HTTP Messages"
date: "2019-12-27 16:00:00 UTC"
tags:
  - "http messages"
  - "http requests"
  - "http responses"
  - "http"
---

# What Are HTTP Messages?
I worked as a frontend web dev for the past 2 years, that means that I'm only playing around with the data that was already provided to me.
2 months ago, my friend has offered me a contract at his company as a backend dev, and my first task was working on an [authenication server](https://github.com/curveball/a12n-server) for an open-source project [framework](https://github.com/curveball) the team is building. When I was a frontend dev, these data was just there for me, "magically", waiting for me to use them, but now I have to build them from scratch.
This post is about what I've learned about HTTP messages.

## Overview of HTTP messages
The project I was working on was written with RESTful environment, meaning CRUD functionality I was using corresponds with the HTTP methods `POST`, `GET`, `PUT` and `DELETE`. This means that it will use the URI endpoint query for requesting data. As a response, the data will be sent back to you as either success or failure.

I had this 'ah-ha' moment when HTTP messages were explained to me and what requests and responses are consists of.

## HTTP Requests
HTTP Requests are messages sent by the client asking for certain action on the server. They are consists of following elements:

### 1. HTTP Method (GET, POST, PUT, PATCH, DELETE, etc)
When you're requsting from the server, you need to specify what kind of requst you're asking for.
This describes the action to be performed when you're requesting from the server. Will get to details later in the post.
### 2. URL | Path
Usually when you're requesting certain data, it will add queries to the URL.
ie. https://www.examples.com/articles/5
From the example above, after `examples.com/`, it's asking to get the data from article, then asks again to get `5`.

### 3.HTTP Headers
HTTP Headers consists:
1. General headers
2. Request headers
3. Entity Headers
I believe that these are data about the client's current browser setup.
<a href="https://developer.mozilla.org/en-US/docs/Web/HTTP/Messages"><img src="https://media.prod.mdn.mozit.cloud/attachments/2016/08/31/13821/6f88b7d65091c3afafa8e3c04fdc1186/HTTP_Request_Headers2.png" style="max-width: 100%"></a>

### 4.Body (Optional)
When requests are fetching resources, like `GET`, `HEAD`, `DELETE` or `OPTION`, usually don't need a body. Method like `POST` sends data to the server in order to update it.

## HTTP Responses
After you request for you will get the response from the server. HTTP Responses are consists of following elements

### 1.Status Code
You'll get back HTTP status code indicating if the request client sent to the server was a success or failed. There are many different status codes for different cases. I'm not gonna write about them since friend of mine did a post of most of [HTTP status codes](https://evertpot.com/http/).

### 2.Status Message
Status mesasges are usally all tied with what the status code was, and when status code is just a number, status mesasge gives you human readable words for easier understanding of what the status code meant.

* One thing I learened about this as a junior dev though, I always thought this was magically done by the browser, but when I was working on the project, I learned that developer needs to decide which status code to throw depends on the return value you get.

### 2.Headers
Just like reqeusts headers, there are many different headers available that can be divided into several groups:
1. General headers
2. Response headers
3. Entity headers
<a href="https://developer.mozilla.org/en-US/docs/Web/HTTP/Messages"><img src="https://media.prod.mdn.mozit.cloud/attachments/2016/08/31/13823/0a5a12cef96993c8d6fa843d7230a9d9/HTTP_Response_Headers2.png" style="max-width: 100%"></a>

### 3.Body (Optional)
Also not all responses have one, usually if it's a status code with `201` or `204` etc won't have one.

## What did I learn so far?
I never knew what HTTP messages really means or what it does. Not that I know everything about HTTP messages now or I'm even close to being good at it, I understand that the HTTP messages are just how the client and the server communicates with each other to exchange data.

## What should I talk about next?
Since `GET`, `POST`, `PUT`, `PATCH`, `DELETE` all sends different request body, response status & response body, I'd like to take a shot at explaning how each of them are different.