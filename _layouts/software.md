---
layout: default
---

This page is for a <a href="/">Universe Software</a> package.

<h1>{{ page.display_name }}</h1>

{{ page.description }}

<h2>Ways to Run</h2>

{% if page.platforms contains "web" %}
    <h3>Web Browser</h3>

    You can run this app right here in your web browser

    {% if page.web_features != "" %}
        <ul>
        {% if page.web_features contains "offline" %}
            <li>You can use the web app offline.</li>
        {% endif %}
        {% if page.web_features contains "a2hs" %}
            <li>You can add the web app to your home screen/start menu/Launchpad and it will open in a separate window like a normal app.</li>
        {% endif %}
        </ul>
    {% endif %}

    <a class="btn btn-block btn-primary" href="{{ page.web_url }}">
        <span class="float-left">
            <i class="fas fa-crome"></i>
            <i class="fas fa-firefox"></i>
            <i class="fas fa-edge"></i>
            <i class="fas fa-safari"></i>
        </span>
        Open in Web Browser
    </a>
{% endif %}

{% if page.platforms contains "windows" or if page.platforms contains "linux" or if page.platforms contains "android" %}
    <h3>Downloads</h3>

    {% if page.platforms contains "windows" %}
        <a class="btn btn-block btn-primary" href="{{ page.name }}.windows.html">
            <i class="fas fa-windows float-left"></i>
            Windows
        </a>
    {% endif %}

    {% if page.platforms contains "linux" %}
        <a class="btn btn-block btn-primary" href="{{ page.name }}.linux.html">
            <i class="fas fa-linux float-left"></i>
            Linux
        </a>
    {% endif %}

    {% if page.platforms contains "android" %}
        <a class="btn btn-block btn-primary" href="{{ page.apk_url }}">
            <i class="fas fa-android float-left"></i>
            Android
        </a>
    {% endif %}
{% endif %}