---
layout: page
title: Contact Us
description: Get in touch with our team. We're here to help!
permalink: /contact/
custom_css: /assets/css/contact.css

hero:
  topper: "Contact Us"
  title: "Get In Touch With Our Team"
  text: "We're here to help with any questions you may have. Fill out the form below and we'll get back to you as soon as possible."
  background:
    desktop: "/assets/images/construction.jpg"
    mobile: "/assets/images/construction-m.jpg"
    alt: "contact us"

contact:
  topper: "Contact Information"
  title: "How Can We Help?"
  text: "Please fill out the form and we will get back to you as soon as possible. For immediate assistance, please call us directly."
  info:
    - type: "Phone"
      icon: "/assets/svgs/phone.svg"
      link_type: "tel"
      link_value: "{{ site.data.client.phoneForTel }}"
      display_value: "{{ site.data.client.phoneFormatted }}"
    - type: "Email"
      icon: "/assets/svgs/email.svg"
      link_type: "mailto"
      link_value: "{{ site.data.client.email }}"
      display_value: "{{ site.data.client.email }}"
    - type: "Address"
      icon: "/assets/svgs/pin.svg"
      link_type: "map"
      link_value: "{{ site.data.client.address.mapLink }}"
      display_value: "{{ site.data.client.address.lineOne }}, {{ site.data.client.address.lineTwo }}, {{ site.data.client.address.city }}, {{ site.data.client.address.state }} {{ site.data.client.address.zip }}"

map:
  topper: "Our Location"
  title: "Find Us On The Map"
  text: "We're conveniently located in {{ site.data.client.address.city }}, {{ site.data.client.address.state }}. Stop by our office or give us a call to schedule an appointment."
  embed_url: "https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3067.7392352239356!2d-104.98760548462448!3d39.73890797944928!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x876c7ed68bc8aa09%3A0x1e8a29beba7f5f8e!2s1600%20Broadway%2C%20Denver%2C%20CO%2080202!5e0!3m2!1sen!2sus!4v1620508868578!5m2!1sen!2sus"
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
<!--                 Contact Form                 -->
<!-- ============================================ -->

<section id="contact-form">
    <div class="cs-container">
        <div class="cs-content">
            <div class="cs-flex-group">
                <span class="cs-topper">{{ page.contact.topper }}</span>
                <h2 class="cs-title">{{ page.contact.title }}</h2>
                <p class="cs-text">
                    {{ page.contact.text }}
                </p>
                <ul class="cs-ul">
                    {% for item in page.contact.info %}
                    <li class="cs-li">
                        <picture class="cs-icon-wrapper">
                            <img class="cs-icon" aria-hidden="true" src="{{ item.icon }}" alt="{{ item.type | downcase }} icon" width="24" height="24" loading="lazy" decoding="async">
                        </picture>
                        <div class="cs-flex-group">
                            <span class="cs-header">{{ item.type }}</span>
                            {% if item.link_type == 'tel' %}
                            <a href="tel:{{ item.link_value }}" class="cs-link">{{ item.display_value }}</a>
                            {% elsif item.link_type == 'mailto' %}
                            <a href="mailto:{{ item.link_value }}" class="cs-link">{{ item.display_value }}</a>
                            {% elsif item.link_type == 'map' %}
                            <a href="{{ item.link_value }}" target="_blank" class="cs-link">{{ item.display_value }}</a>
                            {% endif %}
                        </div>
                    </li>
                    {% endfor %}
                </ul>
            </div>
        </div>
        <form id="cs-form" name="Contact Form" method="post" data-netlify="true">
            <div class="cs-container">
                <!-- Hidden input used to detect form submissions by bots (Honeypot Field) -->
                <input class="cs-hidden" type="text" name="_honey" style="display:none;">
                <!-- Prevents submissions from opening a new page -->
                <input type="hidden" name="_captcha" value="false">
                <div class="cs-row">
                    <!-- First Name -->
                    <div class="cs-input-group">
                        <label class="cs-label" for="first-name">First Name</label>
                        <input class="cs-input" required type="text" id="first-name" name="first-name">
                    </div>
                    <!-- Last Name -->
                    <div class="cs-input-group">
                        <label class="cs-label" for="last-name">Last Name</label>
                        <input class="cs-input" required type="text" id="last-name" name="last-name">
                    </div>
                </div>
                <div class="cs-row">
                    <!-- Email -->
                    <div class="cs-input-group">
                        <label class="cs-label" for="email">Email</label>
                        <input class="cs-input" required type="email" id="email" name="email">
                    </div>
                    <!-- Phone -->
                    <div class="cs-input-group">
                        <label class="cs-label" for="phone">Phone</label>
                        <input class="cs-input" required type="tel" id="phone" name="phone">
                    </div>
                </div>
                <!-- Message -->
                <div class="cs-input-group">
                    <label class="cs-label" for="message">Message</label>
                    <textarea class="cs-input cs-textarea" required name="message" id="message"></textarea>
                </div>
                <!-- Submit Button -->
                <button class="cs-button-solid" type="submit">Submit Message</button>
            </div>
        </form>
    </div>
</section>

<!-- ============================================ -->
<!--                    Map                       -->
<!-- ============================================ -->

<section id="map">
    <div class="cs-container">
        <div class="cs-content">
            <span class="cs-topper">{{ page.map.topper }}</span>
            <h2 class="cs-title">{{ page.map.title }}</h2>
            <p class="cs-text">
                {{ page.map.text }}
            </p>
        </div>
        <div class="cs-map-wrapper">
            <iframe class="cs-map" src="{{ page.map.embed_url }}" width="600" height="450" style="border:0;" allowfullscreen="" loading="lazy"></iframe>
        </div>
    </div>
</section> 