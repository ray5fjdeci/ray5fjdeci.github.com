---
layout: post
categories: ideas
excerpt: >
  I use Google Forms alot, primarily to track my finances (and also with calorie counting). One quirk is that they don't have an offline solution &mdash; I'm wondering if there are other people out there that find that valuable enough to pay for.
---
*Note: I actually ran this experiment about 2 weeks before I posted this, but wanted to document everything here &mdash; hence this post*

Alright, let's hit another idea and see what we can learn. This one goes like so:

> A forms app that works on mobile and is offline. Maybe include an Android widget so you can tap, tap, done.

A subscription service, that offers the ability to submit Google Forms offline. I use GForms alot, and I'm betting there's others out there that do too (how many there are remains a question that needs answering).

Having the ability to submit forms offline means people that use it for expense tracking can do so painlessly, and from anywhere — those that use it for any other sort of mobile tracking can do the same. It would be very useful to a small set of people that (a) use Google Forms frequently and (b) are on the move.

Frankly, I have no idea how the heck people could possibly use this (and indeed, if anyone would want to use this thing) — hence, the experiment. All I know is that there are many, many users of Google products and if even a small subset of those will find this beneficial, then there's plenty of room to make a business here.

## Approach to Validation

### Landing Page

This time I didn't use the Business Model Canvas like last time, since I don't know what the use-case (and hence, the market) is for this product. Instead, I'll use a landing page showing this feature &mdash; and launch it on HackerNews / ProductHunt. That way, I'll guage the response and create a specific product based on the feedback.

Essentially, what I'll do is:
1. Create a simple landing page showing the main feature
2. Launch it on HackerNews / ProductHunt
3. Reach out to signups and ask them why they signed up
4. Create a specific product based on feedback

I hand-coded the landing page, though that turned out to be a very time-consuming process (especially having to make sure everything looked well on desktop and mobile). It would've made more sense to simple use [one](http://unbounce.com) [of](http://instapage.com) [the](http://optimizely.com) [many](http://wix.com) landing page tools.

Here's what I came up with:

![Landing Page](/assets/landing-page-gforms.png)

And once you hit the "Try it" button, you get a simple modal:

![Modal](/assets/modal-gforms.png)

When you press the "How it Works", it cycles through a series of device screenshots that demonstrate the apps functionality.

![Screens](/assets/landing-page-gforms-screens.png)

The emails are submitted to a Google Firebase database so the whole page is static. I then booked the domain [formsapp.me](http://formsapp.me) and put it up (using [Dokku](https://github.com/dokku/dokku), a roll-your-own Heroku solution).

### Launching the experiment

Before launching, I had to set a clear goal for what the target response rate would be.

The figures I put down were:
- Target visitor count: 1,000 visits
- Target conversion rate to subscriber: 20% (since it's free)

With that out of the way, it was time to launch the landing page. I chose HackerNews and ProductHunt as my channels of choice &mdash; since that's where the most likely target customer base lies.

#### HackerNews

This was simple enough:

![Hacker News submission](/assets/landing-page-gforms-hackernews.png)

I [submitted it](https://news.ycombinator.com/item?id=14580353) on Sunday afternoon.

#### ProductHunt

This was a bit more involved. I had to submit the screenshots of the (make-believe) mobile app along with an icon. I noticed that GIF images were more likely to grab attention, so I made one quickly to go along with the page.

You can find the submission [here](https://www.producthunt.com/posts/formsapp):

![ProductHunt submission](/assets/landing-page-gforms-producthunt.png)

## Results

I waited for 24 hours, and then checked Google Analytics for results:

![Google Analytics](/assets/gforms-analytics-result.png)

Not bad. I managed to score 2,000 visits in total after just 1 day. I also checked the database, but that was much less encouraging: I only managed to get 14 emails.

That meant a dismal conversion rate of 14 / 2000 = 0.7% (a far cry from the 20% rate I'd set). And I wasn't even asking for any money..

Not encouraging.

Still, I decided I'd reach out to the 14 emails and ask them for their feedback. I sent out to the following email to the folks that signed up:

![Email](/assets/gforms-email.png)

I managed to get several responses from the people I reached out, a total of 5 of the 14 responded &mdash; and all of them said that they were B (just curious).

Great.

## Verdict

The numbers have spoken — this idea is officially dead.

