---
layout: post
title: "Why you should be using static site generators with your Neocities"
date: 2026-03-09
tags: [tutorial, jekyll]
category: tutorial
---
Hi everypony! I'd like to promote some propaganda towards static site generators. Some common ones also include: Eleventy, Hugo, and Astro. I personally use Jekyll, which will be what I will be referencing throughout.

I was actually first inspired to use Jekyll from a [blog post](https://melankorin.net/blog/2023/06/19/) by a super cool webmaster, [melankorin](https://melankorin.net), who previously used Jekyll to build their site but currently uses Eleventy / 11ty. They mentioned that having Jekyll was one of the only reasons they kept their blog running, and I was intrigued, to say the least! I looked up tutorials on how to set it up, and here it is, right now. In fact, this blog system is pretty much carried by Jekyll!

---

### 1. Layouts
Layouts are probably the #1 function of static site generators. You know how, when you start a new page, you have to add `<html>`, `<head>` with all that metadata junk? Well, obviously you could always choose to just copy and paste that, but you're lazy! How are you supposed to feel motivated making 500 blog posts if you have to format all that stuff?

Well, that's where layouts come into play. Adding a `_layouts` folder into your project directory, we can make various templates. Let's make a default template `default.html` as an example.

```html
{% raw %}
<!-- _layouts/default.html -->
<!DOCTYPE html>
<html>
    <head>
        <title>{% if page.title %}{{ page.title }} — {% endif %}my site</title>
    </head>
    <body>
        {{ content }}
    </body>
</html>
{% endraw %}
```

---

### 2. Layouts (extended) - Variable edition
Another thing you can do with layouts, other than pasting the same code all over again, is to create variables that make your life easier. For anyone who's taken at least one computer science class, you've probably heard of variables, where they can store information. With Jekyll, you can create variables to use onto your layouts. Then, in your actual `.html` / `.md` file, you can write `variable-name: whatever you want` on top.

For instance, let's say I have `<title>` in my layout. Back in `main.html`, I can write `title: my page title` here. It just helps a lot with readability, or if you want the same formatting but need different words.

Here's some visualisation with `main.html`:
```html
{% raw %}
---
title: my page title
---

Welcome to my main page!
{% endraw %}
```

---

### 3. Layouts (extended extended) - Markdown edition
Have you ever worked with Rentry? If you have, then you're familiar with markdown. It's a way to write paragraphs without typing `<h1>` or `<p>` a million times. Jekyll automatically transforms `.md` files into `.html` when you build your site.

So a blog post like this...

```markdown
{% raw %}
---
title: my cool post
---

## heading

regular text with **bold**
{% endraw %}
```

...becomes a full HTML page using your layout!

---

### 4. Locally hosting (finally not about layouts...)
If you build your website directly onto Neocities, there's a chance you've made a small edit on the site, but had to wait quite a while for the changes to take effect. With Jekyll, you can host your website locally (in other words, test it and see what it looks like) before you upload it onto Neocities. 

I won't go into details on how to install Jekyll properly, but in short--to do that, first, go on your terminal. You should type `cd (your folder path)` to open the folder. Afterwards, type in `bundle exec jekyll serve`. This builds your website, which you can check on any browser with `localhost:4000` (default). Whenever you make changes, you can simply refresh the page, it won't take forever to see results.

Then, you can copy all of your files onto Neocities, or deploy it automatically with Github, which conveniently, I've made a [tutorial]({% post_url 2026-03-09-github-neocities-deployment %}) right in this blog.

---

### Ending note
Again, I won't be going into too much detail on how to set up Jekyll on your laptop, but here's a tiny list of some things you'll need before starting:
1. Ruby installed (Jekyll needs it!)
2. A terminal (don't be scared, we're just typing 3 commands)
3. Your Neocities site folder

And... I guess, that's pretty much it! Why don't you try it out for yourself? Maybe it'll be as useful to you as it did to me!