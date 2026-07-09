---
layout: post
title: "Cradle to Crayon: A journey of growth and development"
date: 2021-05-02 00:00:00 -0700
categories: ["Cradle to crayon"]
tags: []
permalink: /cradle-to-crayon-a-journey-of-growth-and-development/
comment_count: 0
---

![Cradle to Crayon](/assets/images/Cradle-to-crayon.jpg)

### We WELCOME you to our little world: Cradle to Crayon

Meet Sophie, 8 year old and Ryan who is just 4 year old. They both are siblings are children to [Tanya and Tanmay.](https://www.enrichingearlylearning.com/tanya-and-tanmays-corner-a-fun-filled-exciting-parenting-journey/) Here at Cradle to Crayon, we aim to share about their early childhood growth and development with parents and educators across the globe.

Both Sophie and Ryan were raised in a nuclear family. Tanya and Tanmay had always been passionate about their children and thus they ensured providing them with all the required resources and age appropriate activities. They were well stimulated in their early years ensuring holistic development in every way.

At Cradle to Crayon, you can simply expect to get expert tips about child development, free resources to help support the children's growth and development, age appropriate activities and resource ideas and much more derived from the journey of Sophie and Ryan right from the time when they were in Cradle to the time when they started using their crayons.

If you are parent or educator to young child and you are seeking any specific resource or answer to a question, you may leave a comment below the BLOG and we will try to get back on that in our next month's Blog.

Meanwhile you can read some of the blogs from this corner and learn something new today to implement with children at home or in the classroom:

<style>
.link-card-grid{display:grid;grid-template-columns:repeat(auto-fill,minmax(260px,1fr));gap:14px;margin:24px 0 32px;}
.link-card{display:flex;align-items:center;gap:14px;padding:16px 18px;background:#fff;border:1px solid #EDEDED;border-radius:14px;text-decoration:none !important;transition:border-color 0.2s,transform 0.2s,box-shadow 0.2s;}
.link-card:hover{border-color:#76C5C9;transform:translateY(-2px);box-shadow:0 8px 20px rgba(0,103,111,0.08);}
.link-card-num{flex-shrink:0;width:30px;height:30px;border-radius:50%;background:#E4F1F2;color:#00676F;font-weight:700;font-size:12.5px;display:flex;align-items:center;justify-content:center;}
.link-card-title{font-size:14px;font-weight:600;color:#00676F;line-height:1.4;}
</style>

<div class="link-card-grid">
{% assign cat_posts = site.categories["Cradle to crayon"] | sort: 'date' %}
{% assign i = 0 %}
{% for post in cat_posts %}{% unless post.url == page.url %}{% assign i = i | plus: 1 %}<a class="link-card" href="{{ post.url }}"><span class="link-card-num">{{ i }}</span><span class="link-card-title">{{ post.title }}</span></a>
{% endunless %}{% endfor %}
</div>
