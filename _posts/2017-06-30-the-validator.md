---
layout: post
categories: ideas
excerpt: >
  I found it very time consuming to test out the last 2 ideas, and I'm wondering if there's a quicker way to do that specifically for testing out product ideas. That's what I'll be testing with this experiment.
---

The [GForms's Landing page]({% post_url 2017-06-29-the-gforms-idea %}) took me about 10 days to build, launch and validate — most of it spent on the damn front-end making sure everything looked OK on mobile and desktop. Once I ran the experiment, within 24 hours I knew it was not going to fly. The question is, could I have finished it sooner?

You bet.

This idea is to make a simple tool that helps you validate an idea quickly. No more slogging through creating a landing page, hooking up Intercom, etc. A/B testing messaging and running experiments. This tool has all the best practices built-in, and makes the process smooth as silk. $99/month, and you'll still save so much time and money!

That's the idea anyway. Let's see if it picks up any steam.

## Approach to Validation

Step one, as ever, is to validate your riskiest assumption. Let's break out the busines model canvas.

### Business Model Canvas

![Business Model Canvas](/assets/business-model-canvas-validate.png)

### Landing Page

Ok, with that out of the way it's clear that I'm going to need a landing page to test things out. I decided to build it using a landing page builder (as opposed to hand-coding it, which took forever [last time]({% post_url 2017-06-29-the-gforms-idea %})). I settled on [InstaPage](http://instapage.com), and was able to get familiar with it pretty quickly.

The process went like so:
1. Open up Google Docs and type up the copy for the page.
2. Sketch the layout on paper
3. Implement it in InstaPage (I also used Mailchimp for collecting emails)
4. Buy a domain (I used [validate.tech](http://validate.tech) for this experiment)

It was all super-quick, and took just a few hours to put together.

Here's the end result (Yeah, I know &hellip; super-long, and text-heavy):

![Landing Page - Validate](/assets/landing-page-validate.png)

You'll notice a Login link there (that's fake, and leads to an empty page with a fake login screen that does nothing) and an address (also fake).

### Launching the experiment

Again, we need to make sure we've got clear goals ahead of the experiment. Mine was:
- Target visitor count: 1,000 visits
- Target conversion rate to payer: 1% (so, 10 * $49/mo. minimum = $490/mo.)

I didn't have a payment flow setup, it would just ask for your email and then say "Thanks!" before you had a chance to pay &mdash; but it does show intent to pay, which is what I care about right now.

#### HackerNews &amp; ProductHunt

- Hackernews link [here](https://news.ycombinator.com/item?id=14654999)
- ProductHunt link [here](https://www.producthunt.com/posts/validate)

This time, the results were pretty dismal from both channels &hellip; the grand total was: 

![Analytics](/assets/analytics-validate-1.png)

51 visitors; 0 conversions. Damn, that's horrible. The Google Forms idea raked in 1,000 visits per channel (2k visitors total) so I was expecting something similar. However, it seems that was naive &mdash; many people thought that the Google Forms idea was an *actual Google product*, and hence the interest. This idea didn't have that going for it, so no free ride.

Hmm. I need to figure out a way to get more traffic so that the results are at least statistically significant. 

#### Reddit &amp; everything else

In a bid to get more visits, I made sure to submit it everywhere where my target audience might hang out. This included:

- [r/programming](https://www.reddit.com/r/programming/comments/6khslc/test_your_startup_idea_in_under_24_hours/)
- [Software Engineering @ StackExchange](https://softwareengineering.stackexchange.com/questions/351961/how-can-i-effectively-test-a-product-idea-before-building-it) &mdash; yes, I posted a question linking to my site so folks would click it. Shoot me.

This won't get me to 1,000 visits. Instead of spending money to get more visits (via ads), I decided to maximize the data I get per visit. I added [CrazyEgg](http://crazyegg.com) for both heatmaps (which they are well known for), as well as a new feature they'd launched called Recordings (which record everything the user does on your site). Here's what that looks like:

![Recordings](/assets/crazyegg-recordings-validate.png)

Excellent. I waited till the next day for the results to come in:

![Google Analytics - Take 2](/assets/analytics-validate-2.png)

Ok, so that's 100 more visits since yesterday. When digging through the CrazyEgg logs, I noticed something interesting:

![Clicks on Try Validate](/assets/analytics-try-clicks.png)

Looks like 5% of visitors were interested in "Try Validate", a button I'd added at the bottom of the page that simply scrolls up to the pricing section. Hmm, maybe a free trial would've converted better than &hellip; well, nothing.

I then checked the leads, and was surprised to see one lead:

![Leads](/assets/leads-validate-one.png)

Hmm, using a Gmail address for an enterprise plan does not seem promising &mdash; but hey, I sent an email out to Joe anyway to see why he signed up for a demo.

Technically, that makes for a conversion rate of 1 / 150 = ~0.7% vs the goal of 1% &mdash; but again, this depends on how this Joe lead turns out. I'm (hopelessly?) optimistic it'll pan out.

## Results

Update: By the next day, I had 300+ visitors total (most of it from Reddit/programming). No improvement in leads though &mdash; still just the 1.

![Analytics - Final](/assets/analytics-validate-3.png)

The numbers speak for themselves &mdash; this experiment failed.
