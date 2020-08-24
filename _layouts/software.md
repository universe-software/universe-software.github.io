---
layout: default
---

<link rel="stylesheet" href="/assets/css/bootstrap.css" />
<link rel="stylesheet" href="/assets/css/fontawesome.css" />

This page is for a [Universe Software](/) package.

# {{ page.display_name }}

{{ page.description }}

## Ways to Run

{% if page.platforms contains "web" %}
    ### Web Browser

    You can run this app right here in your web browser

    {% if page.web_features != "" %}
        {% if page.web_features contains "offline" %}
            * You can use the web app offline.
        {% endif %}
        {% if page.web_features contains "a2hs" %}
            * You can add the web app to your home screen/start menu/Launchpad and it will open in a separate window like a normal app.
        {% endif %}
    {% endif %}

    <a class="btn btn-block btn-primary" href="{{ page.web_url }}">
        <span class="float-right">
            <i class="fas fa-crome"></i>
            <i class="fas fa-firefox"></i>
            <i class="fas fa-edge"></i>
            <i class="fas fa-safari"></i>
        </span>
        Open in Web Browser
    </a>
{% endif %}

{% if page.platforms contains "windows" or if page.platforms contains "linux" or if page.platforms contains "android" %}
    ### Downloads

    {% if page.platforms contains "windows" %}
        <a class="btn btn-block btn-primary" href="{{ page.name }}.windows.html">
            <i class="fas fa-windows float-right"></i>
            Windows
        </a>
    {% endif %}

    {% if page.platforms contains "linux" %}
        <a class="btn btn-block btn-primary" href="{{ page.name }}.linux.html">
            <i class="fas fa-linux float-right"></i>
            Linux
        </a>
    {% endif %}

    {% if page.platforms contains "android" %}
        <a class="btn btn-block btn-primary" href="{{ page.apk_url }}">
            <i class="fas fa-android float-right"></i>
            Android
        </a>
    {% endif %}
{% endif %}