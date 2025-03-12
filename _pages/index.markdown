---
title: Pixel Perfect Websites
permalink: "/"
description: Meta description for the page
layout: default
custom_css: "/assets/css/local.css"
preloadImg: "/assets/images/landing.jpg"
hero:
  topper: mountain hiking society
  title: Explore the World with Exciting People
  text: Tincidunt lobortis feugiat vivamus at augue eget arcu dictum varius. Nibh
    tortor id aliquet lectus proin nibh condimentum.
  button1:
    text: Explore More
    link: "/about"
    class: cs-button-solid
  button2:
    text: Get in Touch
    link: "/contact"
    class: cs-button-transparent
    icon: https://csimg.nyc3.digitaloceanspaces.com/Hero/play.svg
  background:
    desktop: "/assets/images/landing.jpg"
    mobile: "/assets/images/landing-m.webp"
    alt: new home
about:
  topper: About Us
  title: About Company Title
  text1: In consequat tincidunt turpis sit amet imperdiet. Praesent Class officelan
    nonatoureanor mauris laoreet, iaculis libero quis. Curabitur et tempus eri consequat
    tincidunt turpis sit amet imperdiet. Praesent nonatourean olei aptent taciti sociosqu
    ad litora torquent per.
  text2: In consequat tincidunt turpis sit amet imperdiet. Praesent Class officelan
    nonatoureanor mauris laoreet, iaculis libero quis. Curabitur et tempus eri consequat
    tincidunt turpis sit amet imperdiet. Praesent nonatourean olei aptent taciti sociosqu
    ad litora torquent per.
  quote:
    text: In consequat tincidunt turpis sit amet imperdiet. Praesent Classei consequat
      tincidunt turpis sit amet imperdiet for mind.
    name: Justin Time
    job: CEO-Founder
    icon: https://csimg.nyc3.digitaloceanspaces.com/SideBySide/quote-white.svg
  button:
    text: More About Us
    link: "/about"
  image1:
    desktop: "/assets/images/cabinets2.jpg"
    mobile: "/assets/images/cabinets2-m.jpg"
    alt: cabinets
  image2:
    desktop: "/assets/images/construction.jpg"
    mobile: "/assets/images/construction-m.jpg"
    alt: house
seo:
  topper: SEO Ranking
  title: Talk about a main service keyword
  text1: In consequat tincidunt turpis sit amet imperdiet. Praesent Class officelan
    nonatoureanor mauris laoreet, iaculis libero quis. Curabitur et tempus eri consequat
    tincidunt turpis sit amet imperdiet. Praesent nonatourean olei aptent taciti sociosqu
    ad litora torquent per.
  text2: Lorem, ipsum dolor sit amet consectetur adipisicing elit. Non tenetur, iure
    nihil ipsam qui atque commodi id voluptatem nesciunt, quis animi fuga cum doloribus!
    Eaque laboriosam, unde consectetur iure asperiores ullam. Consequuntur debitis
    a voluptatibus vitae optio autem explicabo quia neque est quas, in placeat. Lorem
    ipsum dolor sit amet consectetur adipisicing elit. Doloribus modi laudantium voluptatibus
    rem libero error minus quia eligendi sapiente eos.
  button:
    text: Read our Blog
    link: "/blog"
  image1:
    desktop: "/assets/images/construction.jpg"
    mobile: "/assets/images/construction-m.jpg"
    alt: house
  image2:
    desktop: "/assets/images/cabinets2.jpg"
    mobile: "/assets/images/cabinets2-m.jpg"
    alt: cabinets
gallery:
  topper: Our Portfolio
  title: Et orci volutpat, back up generator installations
testimonials:
  topper: Our Reviews
  title: Words From Our Customers
  text: Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sit dolor volutpat
    porttitor sagittis nunc nisl. Sagittis sit pellentesque gravida viverra. Leo ut
    sed euismod tortor risus et. Ornare non neque, leo, ornare. Lorem ipsum dolor
    sit amet.
cta:
  title: Get in Touch
  text: Serving the entire state of Colorado and the continental United States. Give
    us a call or fill out the contact form and we'll get back to you as soon as possible.
  button:
    text: Contact Us
    link: "/contact"
  background:
    desktop: "/assets/images/cabinets2.jpg"
    mobile: "/assets/images/cabinets2-m.jpg"
    alt: kitchen cabinets
---

<link rel="stylesheet" href="/assets/css/critical.css" />

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
            <a href="{{ page.hero.button1.link }}" class="{{ page.hero.button1.class }}">{{ page.hero.button1.text }}</a>
            <a href="{{ page.hero.button2.link }}" class="{{ page.hero.button2.class }}">
                {% if page.hero.button2.icon %}
                <img
                class="cs-img"
                loading="lazy"
                decoding="async"
                src="{{ page.hero.button2.icon }}"
                alt="icon"
                width="17"
                height="17" />
                {% endif %}
                {{ page.hero.button2.text }}
            </a>
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
<!--                  Services                    -->
<!-- ============================================ -->

<section id="services" class="services">
    <!-- Get Icons From flaticon.com -->
    {% for service in site.services %}
    <div class="card">
        <picture>
            <img
            aria-hidden="true"
            decoding="async"
            src="{{ service.icon }}"
            alt="{{ service.title }}"
            width="48"
            height="48" />
        </picture>
        <h2>{{ service.title }}</h2>
        <p>{{ service.description }}</p>
    </div>
    {% endfor %}
</section>

<!-- ============================================ -->
<!--                 Side By Side                 -->
<!-- ============================================ -->

<section id="sbs">
    <div class="cs-container">
        <!-- Left Image Section -->
        <div class="cs-left">
            <picture class="cs-picture cs-picture1">
                <source media="(max-width: 600px)" srcset="{{ page.about.image1.mobile }}">
                <source media="(min-width: 601px)" srcset="{{ page.about.image1.desktop }}">
                <img aria-hidden="true" decoding="async" src="{{ page.about.image1.desktop }}" alt="{{ page.about.image1.alt }}" loading="lazy" width="400" height="563">
            </picture>
            <picture class="cs-picture cs-picture2">
                <source media="(max-width: 600px)" srcset="{{ page.about.image2.mobile }}">
                <source media="(min-width: 601px)" srcset="{{ page.about.image2.desktop }}">
                <img aria-hidden="true" decoding="async" src="{{ page.about.image2.desktop }}" alt="{{ page.about.image2.alt }}" loading="lazy" width="400" height="563">
            </picture>
        </div>
        <!-- Right Content Section-->
        <div class="cs-right">
            <span class="cs-topper">{{ page.about.topper }}</span>
            <h2 class="cs-title">{{ page.about.title }}</h2>
            <p class="cs-text">
                {{ page.about.text1 }}
            </p>
            <p class="cs-text">
                {{ page.about.text2 }}
            </p>
            <div class="cs-flex-group">
                <p class="cs-flex-p">
                    {{ page.about.quote.text }}
                </p>
                <span class="cs-name">{{ page.about.quote.name }}</span>
                <span class="cs-job">{{ page.about.quote.job }}</span>
                <img 
                class="cs-quote-icon"
                loading="lazy"
                decoding="async"
                src="{{ page.about.quote.icon }}"
                alt="quote"
                width="136"
                height="77" />
            </div>
            <a href="{{ page.about.button.link }}" class="cs-button-solid">{{ page.about.button.text }}</a>
        </div>
    </div>
</section>

<!-- ============================================ -->
<!--            Extra Content To Rank             -->
<!-- ============================================ -->

<section id="sbs-r">
    <div class="cs-container">
        <!-- Left Image Section -->
        <div class="cs-left">
            <picture class="cs-picture cs-picture1">
                <source media="(max-width: 600px)" srcset="{{ page.seo.image1.mobile }}">
                <source media="(min-width: 601px)" srcset="{{ page.seo.image1.desktop }}">
                <img aria-hidden="true" decoding="async" src="{{ page.seo.image1.desktop }}" alt="{{ page.seo.image1.alt }}" loading="lazy" width="400" height="560">
            </picture>
            <picture class="cs-picture cs-picture2">
                <source media="(max-width: 600px)" srcset="{{ page.seo.image2.mobile }}">
                <source media="(min-width: 601px)" srcset="{{ page.seo.image2.desktop }}">
                <img aria-hidden="true" decoding="async" src="{{ page.seo.image2.desktop }}" alt="{{ page.seo.image2.alt }}" loading="lazy" width="400" height="560">
            </picture>
        </div>
        <!-- Right Content Section-->
        <div class="cs-right">
            <span class="cs-topper">{{ page.seo.topper }}</span>
            <h2 class="cs-title">{{ page.seo.title }}</h2>
            <p class="cs-text">
                {{ page.seo.text1 }}
            </p>
            <p class="cs-text">
                {{ page.seo.text2 }}
            </p>
            <a href="{{ page.seo.button.link }}" class="cs-button-solid">{{ page.seo.button.text }}</a>
        </div>
    </div>
</section>

<!-- ============================================ -->
<!--                   Gallery                    -->
<!-- ============================================ -->

<section id="gallery">
    <div class="cs-container">
        <span class="cs-topper">{{ page.gallery.topper }}</span>
        <h2 class="cs-title">{{ page.gallery.title }}</h2>
        <div class="cs-image-group">
            <!-- Row 1-->
            <div class="cs-row cs-row-1">
                {% for item in site.portfolio limit:3 %}
                <picture class="cs-picture cs-picture{{ forloop.index }}">
                    <source media="(max-width: 600px)" srcset="{{ item.image_mobile }}">
                    <source media="(min-width: 601px)" srcset="{{ item.image }}">
                    <img aria-hidden="true" decoding="async" src="{{ item.image }}" alt="{{ item.title }}" loading="lazy" width="400" height="560">
                </picture>
                {% endfor %}
            </div>
            <!-- Row 2 -->
            <div class="cs-row cs-row-2">
                {% for item in site.portfolio offset:3 limit:3 %}
                <picture class="cs-picture cs-picture{{ forloop.index }}">
                    <source media="(max-width: 600px)" srcset="{{ item.image_mobile }}">
                    <source media="(min-width: 601px)" srcset="{{ item.image }}">
                    <img aria-hidden="true" decoding="async" src="{{ item.image }}" alt="{{ item.title }}" loading="lazy" width="400" height="560">
                </picture>
                {% endfor %}
            </div>
            <!-- Row 3 -->
            <div class="cs-row cs-row-3">
                {% for item in site.portfolio offset:6 limit:3 %}
                <picture class="cs-picture cs-picture{{ forloop.index }}">
                    <source media="(max-width: 600px)" srcset="{{ item.image_mobile }}">
                    <source media="(min-width: 601px)" srcset="{{ item.image }}">
                    <img aria-hidden="true" decoding="async" src="{{ item.image }}" alt="{{ item.title }}" loading="lazy" width="400" height="560">
                </picture>
                {% endfor %}
            </div>
        </div>
    </div>
</section>

<!-- ============================================ -->
<!--                 Testimonials                 -->
<!-- ============================================ -->

<section id="reviews">
    <div class="cs-container">
        <span class="cs-topper">{{ page.testimonials.topper }}</span>
        <h2 class="cs-title">{{ page.testimonials.title }}</h2>
        <p class="cs-text">
            {{ page.testimonials.text }}
        </p>
        <ul class="cs-card-group">
            {% for testimonial in site.testimonials %}
            <li class="cs-item">
                <img class="cs-item-img" aria-hidden="true" loading="lazy" decoding="async" src="{{ testimonial.image }}" alt="person" width="80" height="80" />
                <p class="cs-item-p">
                    {{ testimonial.content }}
                </p>
                <span class="cs-reviewer">
                    {{ testimonial.name }}
                    <span class="cs-desc">{{ testimonial.position }}</span>
                </span>
            </li>
            {% endfor %}
        </ul>
    </div>
</section>

{% include cta.html %}
