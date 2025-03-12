---
title: Blog
permalink: "/blog/"
layout: page
description: Read our latest articles and updates
custom_css: "/assets/css/blog.css"
hero:
  topper: Our Blog
  title: Latest News & Articles
  text: Stay up to date with our latest news, tips, and insights from our team.
  background:
    desktop: "/assets/images/construction.jpg"
    mobile: "/assets/images/construction-m.jpg"
    alt: blog
blog:
  title: All Posts
cta:
  title: Have Questions?
  text: If you have any questions or would like to learn more about our services,
    don't hesitate to get in touch.
  button:
    text: Contact Us
    link: "/contact"
  background:
    desktop: "/assets/images/construction.jpg"
    mobile: "/assets/images/construction-m.jpg"
    alt: construction
---

<!-- ============================================ -->
<!--                    Hero                      -->
<!-- ============================================ -->

<section id="hero">
    <div class="cs-container">
        <div class="cs-flex-group">
            <span class="cs-topper">{{ page.hero.topper }}</span>
            <h1 class="cs-title">{{ page.hero.title }}</h1>
            <p class="cs-text">
                {{ page.hero.text }}
            </p>
        </div>
    </div>

    <!-- Background Image -->
    <picture class="cs-picture">
        <source media="(max-width: 600px)" srcset="{{ page.hero.background.mobile }}">
        <source media="(min-width: 601px)" srcset="{{ page.hero.background.desktop }}">
        <img aria-hidden="true" decoding="async" src="{{ page.hero.background.desktop }}" alt="{{ page.hero.background.alt }}" width="2500" height="1667" loading="eager">
    </picture>
</section>

<!-- ============================================ -->
<!--                 Blog Posts                   -->
<!-- ============================================ -->

<section id="blog-posts">
    <div class="cs-container">
        <div class="cs-content">
            <h2 class="cs-title">{{ page.blog.title }}</h2>
        </div>
        <ul class="cs-card-group">
            {% for post in site.posts %}
            <li class="cs-item">
                <a href="{{ post.url }}" class="cs-link">
                    <picture class="cs-picture">
                        <img class="cs-img" loading="lazy" decoding="async" src="{{ post.image }}" alt="{{ post.image_alt }}" width="370" height="370">
                    </picture>
                    <div class="cs-info">
                        <span class="cs-date">{{ post.date | date: "%B %d, %Y" }}</span>
                        <h3 class="cs-h3">{{ post.title }}</h3>
                        <p class="cs-item-text">
                            {{ post.description }}
                        </p>
                        <span class="cs-read-more">Read More</span>
                    </div>
                </a>
            </li>
            {% endfor %}
        </ul>
    </div>
</section>

<!-- ============================================ -->
<!--                   CTA                        -->
<!-- ============================================ -->

<section id="cta">
    <div class="cs-container">
        <div class="cs-content">
            <h2 class="cs-title">{{ page.cta.title }}</h2>
            <p class="cs-text">
                {{ page.cta.text }}
            </p>
            <a href="{{ page.cta.button.link }}" class="cs-button-solid">{{ page.cta.button.text }}</a>
        </div>
    </div>
    <!-- Background Image -->
    <picture class="cs-background">
        <source media="(max-width: 600px)" srcset="{{ page.cta.background.mobile }}">
        <source media="(min-width: 601px)" srcset="{{ page.cta.background.desktop }}">
        <img loading="lazy" decoding="async" src="{{ page.cta.background.desktop }}" alt="{{ page.cta.background.alt }}" width="1920" height="1280" aria-hidden="true">
    </picture>
</section> 