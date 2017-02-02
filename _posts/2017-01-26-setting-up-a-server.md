---
layout: post
category : Projects
tagline: "| Setting up a VPS"
tags : [VPS, Uni, Linux, PC, Ubuntu, Mail-in-a-box, MIAB]
---

{% include JB/setup %}

After seeing [this website](https://www.privacytools.io) it really got me thinking of my personal privacy and the amount of information being tracked and used against me, especially advertisements that would show in Facebook after reading about similar content on a different website.

I saw that it was possible to roll your own mailbox and it was made simple by [mail-in-a-box](https://mailinabox.email), so I got my geek on and 48 hours later I finally have something that works!

#### Getting a VPS and my own URL (read as Earl)

I checked out the competition for a few VPS providers and ended up using [scaleway](https://www.scaleway.com) due to their low pricing and excellent systems available at such a low price. One VPS with a dual-core 64bit processor, 2GB of RAM and 50GB SSD storage for a pleasant &euro;2.99 (around &pound;2.50) a month and I was off, server creation was simple and quick and I had my own Ubuntu instance running soon enough.

The URL was a tricky one, I've been caught out buying domains and web hosting from go-daddy and domain.com in the past, they have plenty of offers and discounts on the domain name itself but they sting you with a bunch of payments after. I opted for [gandi](https://www.gandi.net), not the prettiest of sites (especially for a web servicing company) but the prices were reasonable and worked out cheaper in the end!

I bought my aworley.uk domain for &euro;9.60 (&pound;8.15) and so all together for a year it's going to cost &pound;38.15 which sounds a lot worse than &pound;3.18 a month, or not buying a muffin and coffee a month with change!

#### Running MIAB set-up

The tutorial video on the website is actually very thorough and useful unfortunately I had an issue with a `packaging not found` error. --Long story short and a lot of wasted time follow [the steps here](https://discourse.mailinabox.email/t/unable-to-run-mailinabox-command/1840/14?u=mada360) and re-run the installation and all will work just fine.-- Update [v0.21c](https://github.com/mail-in-a-box/mailinabox/blob/v0.21c/CHANGELOG.md#changelog) fixes the packaging error.



#### And now to wait

A lot of the DNS stuff takes a long time to ripple through the servers so things will probably not work for a bit (30 minutes-hours) There will probably be the odd error flagged on the admin page, just wait and they should resolve themselves given time.


