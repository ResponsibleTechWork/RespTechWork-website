---
layout: post
title:  "Making responsible decisions when developing this website"
date:   2021-08-10 09:21:00 +0100
excerpt: >-
  The goal of ResponsibleTech.Work is to help all of us make more responsible decisions. When I was developing this website, I found it important to follow responsible principles outlined in the framework and make a number of small decisions to show how websites can be developed more responsibly. 
tags: development
author: alja
---

{{page.excerpt}}

***

In addition to wanting to lead by example, I was motivated by web development practices I noticed while doing research for the framework. On the sustainability side, I found way too many websites that preach about web sustainability on carbon-heavy websites. You know the type, lots of large images, scripts, trackers, pop-ups. And on the other side of the not-so-responsible spectrum, there were the many websites that insisted I should give up my email address to view their supposedly free resources. Why did such practices become commonplace in our industry?

## Responsible web development decisions that should become more common

Given the nature of the project, I knew that this website needs to be different. These are some of the responsible decisions I made that might be considered non-standard in the industry:

* **Using a static site generator to build this website**: WordPress might be the most common choice when building a new website, especially for those unfamiliar with web development. Even though this website has a fair amount of content, it is essentially a simple collection of pages, which has no use for a database in the backend. That's why I chose to build it in [Jekyll](https://jekyllrb.com/), a [static site generator](https://jamstack.org/generators/) that does just what it needs to do and creates low-footprint, fast-loading HTML pages. If we ever need to make managing content easier, we can always add something like [Netlify CMS](https://www.netlifycms.org/) and still avoid the hassle and waste of having to manage a database.
* **Choosing a theme that isn't based on a bulky UI library**: Libraries like Bootstrap made designing websites easier and more accessible but using such libraries usually loads your project with tons of code you'll never use. Yes, it's mostly text, and you can do a lot by using minified files. However, way too often, you end up having to override a lot of the CSS from the library you chose, which isn't efficient and creates waste. That's why I was happy to find a [Jekyll theme by Stackbit](https://github.com/stackbit-themes/libris-jekyll) that doesn't rely on a bulky third-party library and was easy to modify to fit my idea of how the website should look.
* **Focus on text, optimize images**: Text is the most sustainable choice for web content. This blog post could easily have a hi-res stock thumbnail image, but it doesn't – on purpose. While images can add value and make websites easier to process, I intentionally try to avoid using decorative images that don't make content easier to understand. When images are used, SVG and WebP are the preferred formats to reduce file size. We might eventually add some embedded video content to present the content in a different format, but the focus should remain on text, the most accessible and sustainable media format.
* **No Google Analytics, no cookies, no tracking**: As exciting as it would be for me to check on the number of page views and visitor countries, I decided not to include any website analytics. No Google Analytics, no Mixpanel, no Hotjar, no Facebook pixel, no other tracking nonsense. This is an open-source educational website, I don't need to optimize its bounce rate. I don't need to know where you're from. I trust that you'll get in touch if you want to tell us that you found the website useful. Ultimately, hearing direct feedback from a person means so much more than vanity metrics. If I want to know what people think of the website, I'll be forced to talk to actual people, and that's a good thing. And hey, I don't even need to annoy you with cookie warnings because there are none! If you have a good business case for web analytics, please look into more privacy-conscious alternatives like [Fathom](https://usefathom.com/), [Matomo](https://matomo.org/), or others. Google Analytics isn't the only choice!
* **Not forcing you to sign up to read content**: My thinking here is that we should aim to make the content so useful you'll want to tell your friends and coworkers about it and that you're smart enough to figure out how to [subscribe to the newsletter]({{site.news_signup}}) or to the RSS feeds (we have one for new [blog posts]({{site.feed.collections.posts.path}}) and another for the [tools collection]({{site.feed.collections.tools.path}})) if you want to be notified of new stuff. No annoying pop-ups, no unnecessary data collection, less digital waste. 
* **Limiting the use of social networks**: Similarly, you won't find a Facebook page or Instagram profile for this project. I don't think Facebook is doing enough as a company to act responsibly. I did decide to set up a [Twitter account](https://twitter.com/RespTechWork) to offer one additional way to get in touch with us, but we have no need for additional profiles, and there are no internal follower goals. Plus, having fewer social profiles to manage means less work for the team and being able to spend more time developing what matters: the content. Our goal here is to educate, not to boost engagement on some third-party service.
* **Using responsible principles when choosing hosting**: I decided to host the website's source code on GitHub because of its past support of underrepresented communities – among others, the company has sponsored several free programming workshops for women I organized – and their commitment to [social impact](https://socialimpact.github.com). I also appreciate their [decision](https://github.blog/changelog/2020-10-01-the-default-branch-for-newly-created-repositories-is-now-main/) to rename default branches in new repositories as main. Additionally, the company is carbon-neutral, committed to run on 100% renewable energy by 2025, and dedicated to implementing other [sustainability practices](https://github.blog/2021-04-22-environmental-sustainability-github/). Also [committed to sustainability is Netlify](https://www.netlify.com/sustainability/), the service I decided to use to deploy the website.
* **Using responsible principles when choosing other tools**: MailChimp is often the go-to choice when setting up a newsletter. However, I wanted a service that would allow me to turn off email tracking and is possibly also committed to being more responsible. This is how I found [EmailOctopus](https://emailoctopus.com/). In addition to allowing me to turn off *all* tracking (yep, I won't know if you open our newsletter or not because it's none of my business), the company is committed to [doing good](https://emailoctopus.com/doing-good) and building an ethical email marketing community. Upon creating a new account, I was pleasantly surprised to receive an email from the moderation team inquiring about my plan for the list  – and I wasn't able to send out any emails before confirming my good intentions. As a customer, I am actually happy to see that this is a company that adds an extra layer of protection for non-customers before allowing people to send out emails.


On their own, the individual choices on this list might not seem like much. Or maybe they sound like too much effort and compromise. In practice, none of these decisions increased development time – if anything, they made my job easier. Not having to test a bunch of various third-party integrations saved time, and optimizing the website will hopefully keep hosting costs lower in addition to being more sustainable. According to the [Website Carbon Calculator](https://www.websitecarbon.com/), [this website is cleaner than 91% of web pages tested](https://www.websitecarbon.com/website/responsibletech-work/), and about 0.10g of CO2 is produced every time somebody visits the website. A good start, although there are always improvements to be made, as I discuss at the end of this post.

## Why does this matter?

I decided to share my thought process because I firmly believe that we can approach web development differently. Just because everyone uses Google Analytics, it doesn't mean you have to as well – especially if you're not really using the data for anything other than vanity metrics.


Given the impact our industry has on people and the planet, we need to take responsibility for every piece of code we deploy. Even if it is just a simple education website like this. We have to remind ourselves that just because something is digital, it doesn't mean it's clean, green, and better for people.


I'm under no illusion that these small decisions will solve the climate crisis or be enough to support companies that do business differently. But I believe that **we can all make a difference if we collectively decided to make more responsible choices every single day, with every commit**.

## The job isn't done

That said, there are still several things on our to-do list that could further reduce this website's impact:

* **Optimize code**: While I tried to optimize code as much as possible during development, the design is based on a third-party theme, so there's probably still some low-hanging fruits in the shape of unused code laying around.
* **Improve accessibility**: This website's theme has been designed with accessibility in mind, but I haven't done any in-depth accessibility testing other than the basic automated checks.
* **Review hosting supply chain**: There might be more sustainable hosting and domain management options out there, and that's certainly something I'd like to learn more about moving forward.


