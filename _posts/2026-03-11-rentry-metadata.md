---
layout: post
title: "Rentry METADATA cheat sheet"
date: 2026-03-11
tags: [guide, rentry]
category: guide
---

# Before we begin...
Let's talk a little about what metadata is. If you already know, you can skip here for the index.

I basically took [this page from Rentry](https://rentry.co/metadata-how) and formatted it so it's a bit easier to look at and navigate.

Frankly, I also need this cheatsheet, so it's a win-win! Here you go.

## Page

| Metadata | Use | Max length |
|----------|----------|------|
| PAGE_TITLE | Appears on the tab for this page's window in the browser | 60 |
| PAGE_DESCRIPTION | Used by search engines and content snippets | 160 |
| PAGE_IMAGE | Used by search engines and content snippets. If we ever have internal page linking with previews, this is what will show | 1000 |
| PAGE_ICON | Changes the icon that appears in the browser tab | 1000 |

## Share

| Metadata | Use | Max length |
|----------|----------|------|
| SHARE_TITLE | Used by search engines and content snippets | 60 |
| SHARE_DESCRIPTION | Used by search engines and content snippets. It's unlikely to be necessary to set this as well as PAGE_DESCRIPTION | 160 |
| SHARE_IMAGE | Used by search engines and content snippets | 1000 |
| SHARE_TWITTER_TITLE | Used by Twitter and other Twitter compatible platforms as the title snippet of the link | 60 |
| SHARE_TWITTER_DESCRIPTION | Used by Twitter and other Twitter compatible platforms as the description snippet of the link | 160 |
| SHARE_TWITTER_IMAGE | This image will be used for Twitter and other Twitter compatible platforms when loading a preview of this page | 1000 |

## Option

| Metadata | Use | Max length |
|----------|----------|------|
| OPTION_DISABLE_VIEWS | Disables the view counter and hides it. Existing view count will return when this is unset | 5 |
| OPTION_DISABLE_SEARCH_ENGINE | Removes the URL from the sitemap and instructs crawling search engines to not index it. Note that it can take up to 2 months for Google to remove listings | 5 |
| OPTION_USE_ORIGINAL_PUB_DATE | If a URL was deleted and re-created this forces it to show the date it was first published, rather than date of re-activation | 5 |

## Access

| Metadata | Use | Max length |
|----------|----------|------|
| ACCESS_RECOMMENDED_THEME | When a page does not look good in one of the viewing modes, this will auto switch the viewer to the listed mode (dark/light) | 5 |
| ACCESS_EASY_READ | Adds an e2r button next to the high contrast button that people can click on, which will link to the listed URL | 300 |

## Secret

| Metadata | Use | Max length |
|----------|----------|------|
| SECRET_VERIFY | Specify one or more external accounts that you can later use to recover your page if you forget the edit code | 3000 |
| SECRET_RAW_ACCESS_CODE | A passcode that allows access to the raw version of this page, including through an automated script | 100 |
| SECRET_EMAIL_ADDRESS | Supply an email address to attach to this page, which we can then use to manually reset your edit code on request | 300 |

## Safety

| Metadata | Use | Max length |
|----------|----------|------|
| SAFETY_PAGE_WARNING | Adds a warning popup to your page before allowing visitors to view (adult/sensitive/epilepsy/custom) | 100 |
| SAFETY_PAGE_WARNING_DESCRIPTION | Provide your own text to the warning popup created by SAFETY_PAGE_WARNING | 240 |
| SAFETY_MEDIA_BLUR | Blurs all images in your page and requires them to be clicked before showing | 5 |
| SAFETY_LINK_WARNING | Triggers a popup when clicking on a link within your content (adult/epilepsy/sensitive) | 100 |
| SAFETY_LINK_WARNING_DESCRIPTION | Provide your own text to the link warning popup | 240 |
| SAFETY_PAGE_FLAG | Creates a visual icon on your page to inform readers that a page contains certain material (adult/epilepsy/sensitive) | 100 |

## Container

| Metadata | Use | Max length |
|----------|----------|------|
| CONTAINER_PADDING | The internal spacing between the main container and the content | 64 |
| CONTAINER_MAX_WIDTH | Limits and centers the content container's width | 16 |
| CONTAINER_INNER_FOREGROUND_COLOR | Sets the color of the inner foreground (semi-transparent layer on top of content) | 32 |
| CONTAINER_INNER_BACKGROUND_COLOR | Sets the color of the inner background | 32 |
| CONTAINER_INNER_BACKGROUND_IMAGE | Sets the background image used in the inner container, behind the content | 1000 |
| CONTAINER_INNER_BACKGROUND_IMAGE_REPEAT | Controls if/how the background image repeats (no-repeat/repeat-x/repeat-y/round/space) | 16 |
| CONTAINER_INNER_BACKGROUND_IMAGE_POSITION | Controls the position of the inner background image (bottom/center/left/right/top) | 6 |
| CONTAINER_INNER_BACKGROUND_IMAGE_SIZE | Should the image stretch or sit as large as possible without distorting (contain/cover) | 16 |
| CONTAINER_OUTER_FOREGROUND_COLOR | Sets the color for the foreground of the outer container | 32 |
| CONTAINER_OUTER_BACKGROUND_COLOR | Sets the color for the very back of the outer container | 32 |
| CONTAINER_OUTER_BACKGROUND_IMAGE | A link to an image to be used for the outer container's background | 1000 |
| CONTAINER_OUTER_BACKGROUND_IMAGE_REPEAT | Controls whether the outer background image should repeat (no-repeat/repeat-x/repeat-y/round/space) | 16 |
| CONTAINER_OUTER_BACKGROUND_IMAGE_POSITION | Controls the position of the outer background image (bottom/center/left/right/top) | 16 |
| CONTAINER_OUTER_BACKGROUND_IMAGE_SIZE | Controls whether the outer background image should stretch (contain/cover) | 16 |
| CONTAINER_BORDER_IMAGE | The location of the image, stored elsewhere | 1000 |
| CONTAINER_BORDER_IMAGE_SLICE | Controls how the border image should be cut up and displayed | 64 |
| CONTAINER_BORDER_IMAGE_WIDTH | The width of the image used in the border | 64 |
| CONTAINER_BORDER_IMAGE_OUTSET | Controls where the border image appears in relation to the edges of the container | 64 |
| CONTAINER_BORDER_IMAGE_REPEAT | Whether the image repeats or not throughout the border, and how (stretch/repeat/round/space) | 32 |
| CONTAINER_BORDER_COLOR | The color of the border | 120 |
| CONTAINER_BORDER_WIDTH | The thickness of the border | 64 |
| CONTAINER_BORDER_STYLE | The appearance style of the border (dotted/dashed/solid/double/groove/ridge/inset/outset) | 64 |
| CONTAINER_BORDER_RADIUS | Curves the sides of the container | 64 |
| CONTAINER_SHADOW_COLOR | The color of the shadow | 32 |
| CONTAINER_SHADOW_OFFSET | The amount the shadow offsets from the container | 32 |
| CONTAINER_SHADOW_SPREAD | The spread (thickness) of the shadow | 12 |
| CONTAINER_SHADOW_BLUR | The blurryness of the shadow | 12 |

## Content

| Metadata | Use | Max length |
|----------|----------|------|
| CONTENT_FONT | Sets the font for the page content (Google Fonts names with underscores) | 1000 |
| CONTENT_FONT_WEIGHT | Sets the font weight/boldness | 24 |
| CONTENT_TEXT_DIRECTION | Sets text direction (ltr/rtl) | 7 |
| CONTENT_TEXT_SIZE | Sets the font size for different content types | 128 |
| CONTENT_TEXT_ALIGN | Sets how text sits on the page (right/center/justify) | 7 |
| CONTENT_TEXT_SHADOW_COLOR | Sets the color of text shadow | 32 |
| CONTENT_TEXT_SHADOW_OFFSET | Sets the offset of text shadow | 32 |
| CONTENT_TEXT_SHADOW_BLUR | Sets the blur of text shadow | 12 |
| CONTENT_TEXT_COLOR | Sets the base text color | 128 |
| CONTENT_LINK_COLOR | Sets the base link color | 16 |
| CONTENT_BULLET_COLOR | Sets the bullet color for lists | 64 |
| CONTENT_LINK_BEHAVIOR | Sets whether links load in new pages or same page (same/new) | 32 |