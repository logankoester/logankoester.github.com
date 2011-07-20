---
layout: post
title: "FeedzirraRedis"
published: true
---

If you've ever wanted to include some data from an RSS/Atom feed on a page from Ruby, you've probably run into this problem:

It's completely unreasonable to hammer the feed provider with a request every time the page is rendered, but it's no more 
reasonable to use a big relational database like MySQL just to cache some stupid tweets or blog posts, especially if your
application wouldn't otherwise need one.

But apparently this layer of persistance has been deemed out-of-scope by the creators of popular RSS consumer libraries
such as [Feedzirra](https://github.com/pauldix/feedzirra).

So I wrote a little gem called [feedzirra-redis](https://github.com/logankoester/feedzirra-redis/) to take care of this
as transparently as possible. You can use it just like you would [Feedzirra](https://github.com/pauldix/feedzirra) normally,
but your shit doesn't disappear at the end of the script, so you can do the dirty work from a Rakefile via cron instead of
in the web request/response cycle while your users impatiently twiddle their thumbs.

## Installation

    gem install feedzirra-redis

See the [README](https://github.com/logankoester/feedzirra-redis/blob/master/README.markdown) and 
[test suite](https://github.com/logankoester/feedzirra-redis/blob/master/test/test_feedzirra-redis.rb) for example usage.

Enjoy!
