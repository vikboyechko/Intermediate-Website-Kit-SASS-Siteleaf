---
layout: page
title: About Us
description: Learn more about our company and our mission.
permalink: /about/
custom_css: /assets/css/about.css

hero:
  topper: "About Our Company"
  title: "We're Passionate About What We Do"
  text: "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nullam eget felis eget urna consectetur ultrices. Vestibulum ante ipsum primis in faucibus orci luctus et ultrices posuere cubilia curae."
  background:
    desktop: "/assets/images/cabinets2.jpg"
    mobile: "/assets/images/cabinets2-m.jpg"
    alt: "about us"

story:
  topper: "Our Story"
  title: "How We Got Started"
  text1: "In consequat tincidunt turpis sit amet imperdiet. Praesent Class officelan nonatoureanor mauris laoreet, iaculis libero quis. Curabitur et tempus eri consequat tincidunt turpis sit amet imperdiet. Praesent nonatourean olei aptent taciti sociosqu ad litora torquent per."
  text2: "In consequat tincidunt turpis sit amet imperdiet. Praesent Class officelan nonatoureanor mauris laoreet, iaculis libero quis. Curabitur et tempus eri consequat tincidunt turpis sit amet imperdiet. Praesent nonatourean olei aptent taciti sociosqu ad litora torquent per."
  quote:
    text: "In consequat tincidunt turpis sit amet imperdiet. Praesent Classei consequat tincidunt turpis sit amet imperdiet for mind."
    name: "Justin Time"
    job: "CEO-Founder"
    icon: "https://csimg.nyc3.digitaloceanspaces.com/SideBySide/quote-white.svg"
  image1:
    desktop: "/assets/images/cabinets2.jpg"
    mobile: "/assets/images/cabinets2-m.jpg"
    alt: "cabinets"
  image2:
    desktop: "/assets/images/construction.jpg"
    mobile: "/assets/images/construction-m.jpg"
    alt: "house"

values:
  topper: "Our Values"
  title: "What We Stand For"
  text: "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nullam eget felis eget urna consectetur ultrices. Vestibulum ante ipsum primis in faucibus orci luctus et ultrices posuere cubilia curae."
  items:
    - title: "Quality"
      text: "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nullam eget felis eget urna consectetur ultrices."
    - title: "Integrity"
      text: "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nullam eget felis eget urna consectetur ultrices."
    - title: "Innovation"
      text: "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nullam eget felis eget urna consectetur ultrices."

team:
  topper: "Our Team"
  title: "Meet The People Behind Our Success"
  text: "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nullam eget felis eget urna consectetur ultrices. Vestibulum ante ipsum primis in faucibus orci luctus et ultrices posuere cubilia curae."
  members:
    - name: "John Smith"
      job: "CEO & Founder"
      text: "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nullam eget felis eget urna consectetur ultrices."
      image: "/assets/images/person1.jpg"
    - name: "Jane Doe"
      job: "Operations Manager"
      text: "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nullam eget felis eget urna consectetur ultrices."
      image: "/assets/images/person2.jpg"
    - name: "Robert Johnson"
      job: "Lead Designer"
      text: "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nullam eget felis eget urna consectetur ultrices."
      image: "/assets/images/person3.jpg"

cta:
  title: "Ready to Work With Us?"
  text: "Serving the entire state of Colorado and the continental United States. Give us a call or fill out the contact form and we'll get back to you as soon as possible."
  button:
    text: "Contact Us"
    link: "/contact"
  background:
    desktop: "/assets/images/construction.jpg"
    mobile: "/assets/images/construction-m.jpg"
    alt: "construction"
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
<!--                 Side By Side                 -->
<!-- ============================================ -->

<section id="sbs">
    <div class="cs-container">
        <!-- Left Image Section -->
        <div class="cs-left">
            <picture class="cs-picture cs-picture1">
                <source media="(max-width: 600px)" srcset="{{ page.story.image1.mobile }}">
                <source media="(min-width: 601px)" srcset="{{ page.story.image1.desktop }}">
                <img aria-hidden="true" decoding="async" src="{{ page.story.image1.desktop }}" alt="{{ page.story.image1.alt }}" loading="lazy" width="400" height="563">
            </picture>
            <picture class="cs-picture cs-picture2">
                <source media="(max-width: 600px)" srcset="{{ page.story.image2.mobile }}">
                <source media="(min-width: 601px)" srcset="{{ page.story.image2.desktop }}">
                <img aria-hidden="true" decoding="async" src="{{ page.story.image2.desktop }}" alt="{{ page.story.image2.alt }}" loading="lazy" width="400" height="563">
            </picture>
        </div>
        <!-- Right Content Section-->
        <div class="cs-right">
            <span class="cs-topper">{{ page.story.topper }}</span>
            <h2 class="cs-title">{{ page.story.title }}</h2>
            <p class="cs-text">
                {{ page.story.text1 }}
            </p>
            <p class="cs-text">
                {{ page.story.text2 }}
            </p>
            <div class="cs-flex-group">
                <p class="cs-flex-p">
                    {{ page.story.quote.text }}
                </p>
                <span class="cs-name">{{ page.story.quote.name }}</span>
                <span class="cs-job">{{ page.story.quote.job }}</span>
                <img 
                class="cs-quote-icon"
                loading="lazy"
                decoding="async"
                src="{{ page.story.quote.icon }}"
                alt="gavel"
                width="136"
                height="77" />
            </div>
        </div>
    </div>
</section>

<!-- ============================================ -->
<!--                   Values                     -->
<!-- ============================================ -->

<section id="values">
    <div class="cs-container">
        <div class="cs-content">
            <span class="cs-topper">{{ page.values.topper }}</span>
            <h2 class="cs-title">{{ page.values.title }}</h2>
            <p class="cs-text">
                {{ page.values.text }}
            </p>
        </div>
        <ul class="cs-card-group">
            {% for item in page.values.items %}
            <li class="cs-item">
                <h3 class="cs-h3">{{ item.title }}</h3>
                <p class="cs-item-text">
                    {{ item.text }}
                </p>
            </li>
            {% endfor %}
        </ul>
    </div>
</section>

<!-- ============================================ -->
<!--                   Team                       -->
<!-- ============================================ -->

<section id="team">
    <div class="cs-container">
        <div class="cs-content">
            <span class="cs-topper">{{ page.team.topper }}</span>
            <h2 class="cs-title">{{ page.team.title }}</h2>
            <p class="cs-text">
                {{ page.team.text }}
            </p>
        </div>
        <ul class="cs-card-group">
            {% for member in page.team.members %}
            <li class="cs-item">
                <img class="cs-item-img" aria-hidden="true" loading="lazy" decoding="async" src="{{ member.image }}" alt="person" width="300" height="300" />
                <div class="cs-item-info">
                    <h3 class="cs-name">{{ member.name }}</h3>
                    <span class="cs-job">{{ member.job }}</span>
                    <p class="cs-item-text">
                        {{ member.text }}
                    </p>
                </div>
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