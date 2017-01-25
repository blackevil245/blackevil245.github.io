---
layout: post
title:  "[Recipe] Jekyll flavored Github blog with custom domain topping"
date:   2016-01-26 01:30:00 +0200
categories: blog
tags: jekyll github pages domain
---

## Forewords
Github for a long time has been developers's first choice of version control tool. Powerful as it is now, one must know the magic behind the curtain - Jekyll

> [**Jekyll**](https://jekyllrb.com/) is an open-sourced static site  generator built on Ruby. In a nut shell, you prepare your post template in normal html and css, blod contents written in markdown, and Jekyll with transform your contents into multiple templated blog pages.

Github pages was announced a while back, and is one of many solutions to replace old fashioned CMS(s) such as Wordpress. Not having such big resources pool as other CMS, Jekyll is still favorited by many tech blogger for its simplicity, content-centered blogs.

**Note** This blog is writted with the assumption that you have your blog page ready-made with Jekyll.

OK enough introduction! Let's get started!

![let's get started]({{ site.url }}/images/cooking.gif)

## Ingredients
- 1 finely made, beautiful jekyll theme,
- 1 bowl of mixed amazing blog contents and fresh ideas,
- 50g of cheese and a box of cookies,
- 1 really swag domain
- 1 github repository. It must be named as `yourusername.github.io` or else the food could not be served,
- And the last but not least, a `gh-pages` branch to present the final dish.

## Directions

Prep | Cook | Ready in
--- | --- | ---
`Varies` | `10 mins` | `24 hours`

1. Commit and push your jekyll blog contents to `yourusername.github.io` repository.
2. Go to repository page's setting tab and scroll to github pages settings...

  ![repo-tab]({{ site.url }}/images/repo-tab.PNG)

  ![github-pages-settings]({{ site.url }}/images/github-pages-settings.PNG)

3. From `Source` dropdown, choose the branch that you would like your page to be hosted on. Preferably **gh-pages** branch that we prepared.
4. (Optional) use Github prepared themes if you are not satisfied with your current setup.
5. In `Custom domain` text field, input your awesome domain.
6. Enforce HTTPS will be disabled if you use a custom domain.
7. Press `Save` button next to `Custom domain`.
8. Go to your domain provider, login to their admin dashboard. If you chosen DNS provider does not support customer's admin dashboard, **skip to step 11**. My DNS of choice is [Onlydomains](onlydomains.com) as i got a decent offer for my `.io` domain.
9. After logged into the dashboard, navigate to `DNS settings` for your domain, find the `Zone record` settings.
10. Create 3 new entries as following

  * Host - Type - Content

  ![address-record]({{ site.url }}/images/address-record.PNG)

  * **A** is Address record - **192.30.252.153** and **192.30.252.154** is Github's IP, these are **mandatory** for github to redirect the domain to your github website.
  * **CNAME** is Canonical name record - All request to `example.com` will be served as if it is `www.example.com` and vice versa. This is optional.

11. If your provider does not support dashboard, contact their customer support and ask them to create the same above records for your domain.
12. Voila, setup is now completed. And the foods will be served once your DNS is configured on your provider side.

![food-is-served]({{ site.url }}/images/food-is-served.gif)

## Enjoy!
