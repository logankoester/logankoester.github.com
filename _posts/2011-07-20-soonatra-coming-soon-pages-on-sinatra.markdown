---
layout: post
title: "Soonatra - 'Coming Soon' pages on Sinatra"
published: true
---

## {{ page.title }}

<p class="publish_date"> 20 Jul 2011</p>

I was recently tasked with creating a "coming soon" page for a new project at work. The requirements were the usual:

* Some description of the project features
* A form to signup for an email list / invites
* Display a few posts from an RSS feed
* Show some screenshots of what we're building to collect early feedback

We've also been increasing our focus on A/B testing (aka "split testing"), so I wanted a way to try out different
headlines and see which angle users find most interesting.

This all sounds well and good, but it is very frustrating to take time away from the beginning of an exciting new
project to invest in a page that will only be online for a few short weeks.

I decided I don't ever want to do it again, so I created [Soonatra](https://github.com/agoragames/soonatra).

[Soonatra](https://github.com/agoragames/soonatra) is a simple [Sinatra](http://www.sinatrarb.com/) based framework
for creating these pages quickly.

[Soonatra](https://github.com/agoragames/soonatra) reduces the steps involved to:

* Creating a mailing list (we're using [Mailchimp](http://mailchimp.com/))
* Choosing some colors/graphics that fit well with your brand
* Writing the page copy and setting an RSS feed url.
* Deploy to a free [Heroku](http://heroku.com/) account and parking your domain.

It is easy to extend and manage multiple themes thanks to [Compass](http://compass-style.org/), and does not require a database,
instead using [Redis](http://redis.io/) for RSS feed consumption and tracking A/B test results.

You can fork the git repo and have your site up and running in minutes.

See [README.textile](https://github.com/agoragames/soonatra/blob/master/README.textile) for all the juicy details.
