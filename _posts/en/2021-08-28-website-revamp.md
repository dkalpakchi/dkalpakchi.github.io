---
layout: post
comments: false
lang: en
date:   2021-08-28 10:19:00 +0100
categories: en technical
tags: technical
---
I have started this website in 2017. Back then I just got acquaintained with Jekyll, so styling was quite simple. Now in 2021 the website has finally been revamped thanks to the [Jekyll Chirpy theme](https://github.com/cotes2020/jekyll-theme-chirpy). The major challenge for me was to make it multilingual, since I wanted to write posts both in English and Ukrainian. Unfortunately, Jekyll does not support multilinguality by default, so I had to invent something. Chirpy theme started to support UI multilinguality a couple of months after I've started this whole revamp, but it still does not support multilinguality of posts.

The workaround that I read about somewhere on the net (don't remember the exact source, unfortunately) is to use categories for different languages. So category `en` for English, `uk` foor Ukrainian, etc. Now because one can use many categories, I have added a more explicit parameter `lang` to every post. So the header of each post will look like
```jekyll
---
layout: post
lang: en
date:   2021-08-28 10:19:00 +0100
categories: en technical
---
```

Then I know for sure the language of every page from the `lang` parameter and I can get the posts for each language just by pointing to the respective category page. The translations of categories, tags and some UI elements to different languages are kept in the `_config.yml` under `i18n` field. All I had to do was rewrite a number of includes and layouts of the original Chirpy theme to account for this new `lang` parameter, which was easy enough, so just have a look at [the github repository for this website](https://github.com/dkalpakchi/dkalpakchi.github.io), if you're curious! And voilà, here comes the revamped website!