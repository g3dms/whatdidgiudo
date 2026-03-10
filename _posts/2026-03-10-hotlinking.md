---
layout: post
title: "The hot trend of hotlinking and file hosting"
date: 2026-03-10
tags: [tutorial, images]
category: tutorial
---

Heehee, see what I did there?

...(Crickets)...

...*Anyways*, have you ever been looking through Neocities websites, and seeing sections of website buttons on the side of the page? Buttons (in this context) are usually small, usually animated, images that can link to other web neighbours or cool websites. Obviously someone can just make a hyperlink list of all of that, but that doesn't look particularly pretty. You scroll a bit down, and there's a little message.

> "Please don't hotlink!"

Now, you may be thinking, what even *is* hotlinking? Is it related to an attractive fictional elf that typically dons green clothing? Is it mayhaps risque form of Internet links? That might be a very peculiar sight, but ~~unfortunately~~ no, the true answer is a bit more technical that that.

---

## Can you get to the point already?! What is hotlinking?
Okay, jeez! I'm getting there! Let a guy do some exposition... huhu...

Hotlinking is when you embed a file directly from someone else's server instead of hosting it yourself. You know when you see an image on a forum and the URL looks like `https://files.catbox.moe/abc123.png`? That's a hotlink.

Here's what happens when someone visits that page:

1. Their browser loads the forum page
2. The browser sees that image URL and requests it from Catbox's server
3. Catbox delivers the file, using **their bandwidth**

So instead of:

```html
<!-- hosted yourself, locally -->
<img src="/images/my-cool-picture.jpg">
```

You do:
```html
<!-- the hotlinking method -->
<img src="https://some-other-site.com/images/their-cool-picture.jpg">
```
Essentially, when someone visits your site, their browser grabs the file from the other site!

---

## Why do a lot of people hate it?
Okay, so, imagine you run a website. You pay for hosting, you have bandwidth limits. Then some other site embeds your 5MB wallpaper directly into their post that goes viral. Suddenly you're paying for their traffic, your server slows down, your hosting bill spikes, you get an angry email from your provider, woops.

Since every single view does eat bandwidth from the host, not the site displaying the image, it can get a bit grey at times. This is fine when it's your own files on your own hosting. It's less fine when you're mooching off someone else, and is why people generally don't want you to be hotlinking their stuff. 

There are other problems too:
1. Lack of control — If they delete or change the file, your site breaks
2. Copyright issues — You're displaying someone's work without permission
3. Tracking nightmares — Hotlinked files can leak visitor info via referrer headers

<br>
You can see why some people have an issue with it, especially if they're hosting their own website with a server funded from their own pockets.

---

## Then... why do people still use it?

Well... hotlinking isn't *inherently* evil. It's just a tool. The problem is when you do it to someone who didn't agree to it. 

In fact, there are *lots*, and I mean *lots* of people who hotlink on Neocities. Enter the humble [catbox.moe](https://catbox.moe).

Catbox is a free file hosting service that's been around since 2015. Its service explicitly allows hotlinking. You upload a file, you get a direct link, and you can embed it anywhere. It's funded entirely by donations.

### What Catbox allows

Catbox is pretty generous:
- Files are stored **forever** (unless you use Litterbox for temporary stuff)
- No speed or bandwidth limits
- NSFW content *is* allowed... (within reason—check their banned list)
- Files are 1-to-1 copies—they don't strip metadata or compress anything

### What Catbox doesn't allow

- Commercial CDN usage
- Streaming video for other sites
- Banned file types (.exe, .scr, .cpl, .doc*, .jar)
- Illegal content (obviously)

<br>
And ultimately, this is a game changer for Neocities because of its storage limits. Whether it be busy students, or people trying to save up, sometimes they just can't pay for a larger storage spaces. Instead of storing the actual image files on Neocities (which eat up your precious storage limit), you're just storing lines of text that point to Catbox.

These images typically go for quite a few megabytes (MB), compared to text, which only go for a couple of kilobytes (KB). When you consider 1024 KB = 1 MB, *yes*, it does save a lot of storage.

So yes, I do hotlink my fonts from Catbox. The font you're (probably) reading on right now, Coolvetica, is being hosted on Catbox. I hotlink my images too, sometimes even music.

(Another alternative is [filegarden](https://filegarden.com), which I use for videos, gifs, or when Catbox is down... shh, don't tell anyone!)

---

## What am I supposed to take away from this?
Because I'm sure you all have short attention spans (don't worry, I do too), I'll give you the kind grace of a little something called a TL;DR.

### TL;DR:
- Hotlinking = using someone else's server to host your files
- Bad (boo...) when you do it without permission (bandwidth theft)
- But good (yay!) when you use services designed for it (Catbox, Filegarden, CDNs)
- I use Catbox for fonts/images on this site because Neocities has limits
- Be nice. Don't be a leech. Read the terms!

And that's pretty much it!