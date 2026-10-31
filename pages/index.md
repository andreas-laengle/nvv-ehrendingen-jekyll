---
title: 
layout: page
---

<!--
{% include jumbotron.html heading=site.title text="Create a site from a basic bootstrap template" button-text="Learn More" button-link="ueber-uns.html" %}-->

<div class="row g-0 align-items-stretch my-5">
  <h1 class="mb-4">Herzlich Willkommen beim Natur- und Vogelschutzverein Ehrendingen</h1>
  <p>Liebe Natur- und Vogelfreunde</p>
  <p>Wir begrüssen dich herzlich auf der Homepage des Natur- und Vogelschutzvereins Ehrendingen. Nebst vielerlei Aktivitäten in und um Ehrendingen, alle mit dem Ziel der Hege und Pflege der Tier- und Pflanzenwelt, zu denen jedermann, auch Nichtmitglieder, jederzeit herzlich eingeladen sind, geniessen wir vor allem auch das gemütliche Beisammensein mit Gleichgesinnten.</p>
  <p>Nebst Aktivitäten zu Gunsten der Natur bietet der Natur- und Vogelschutzverein Ehrendingen auch eine einfache Möglichkeit des sich Kennenlernens in unserem Dorf, und das ganz ohne Verpflichtung.</p>
  <p>Nimm ganz unverbindlich an einem unserer nächsten Anlässe teil und lass dich überraschen. Details findest du in unserem JahresprogrammIn neuem Fenster öffnen.</p>
  <p class="my-2"><strong>Der Vorstand</strong></p>
</div>

<h2>Nächster Anlass</h2>

<div class="mt-4 mb-5">
  <table>
    <tr>
      <td style="border: 1px solid #dddddd; text-align: left; padding: 8px; ">
        <strong>Was</strong>
      </td>
      <td style="border: 1px solid #dddddd; text-aligne: left: padding: 8px; ">
        Exkursion Lichtverschmutzung und ihre Auswirkung auf Mensch und Natur
      </td>
    </tr>
    <tr style="background-color: #dddddd">
      <td style="border: 1px solid #dddddd; text-align: left; padding: 8px; ">
        <strong>Wer</strong>
      </td>
      <td style="border: 1px solid #dddddd; text-aligne: left: padding: 8px; ">
        NVV Lengnau
      </td>
    </tr>
    <tr>
      <td style="border: 1px solid #dddddd; text-align: left; padding: 8px; ">
        <strong>Wann</strong>
      </td>
      <td style="border: 1px solid #dddddd; text-aligne: left: padding: 8px; ">
        Donnerstag 29.10.2026
      </td>
    </tr>
    <tr style="background-color: #dddddd">
      <td style="border: 1px solid #dddddd; text-align: left; padding: 8px; ">
        <strong>Wo</strong>
      </td>
      <td style="border: 1px solid #dddddd; text-aligne: left: padding: 8px; ">
        19.00 Uhr beim Parkplatz zwischen Synagoge und Beck Alt in Lengnau.</td>
    </tr>
    <tr>
      <td style="border: 1px solid #dddddd; text-align: left; padding: 8px; ">
        <strong>Dauer</strong>
      </td>
      <td style="border: 1px solid #dddddd; text-aligne: left: padding: 8px; ">
        Rund 2 Stunden
      </td>
    </tr>
    <tr style="background-color: #dddddd">
      <td style="border: 1px solid #dddddd; text-align: left; padding: 8px; ">
        <strong>Spezielles</strong>
      </td>
      <td style="border: 1px solid #dddddd; text-aligne: left: padding: 8px; ">
        Wann haben Sie zum letzten Mal den Sternenhimmel gesehen? Kunstlicht ermöglicht uns Sicherheit, Annehmlichkeiten und wirtschaftliche Entfaltung. Kunstlicht wirkt sich jedoch auch negativ auf das ökologische Zusammenspiel von verschiedenen Tierarten und Pflanzen aus. Roland Bodenmann erklärt uns auf dieser Führung in Lengnau die Auswirkungen von zu viel Licht auf Mensch und Natur und zeigt auf, wie man selber Lichtverschmutzung vermeiden kann.
        <p><strong> Der Anlass ist kostenlos und auch Nichtmitglieder sind herzlich willkommen</strong></p>
      </td>
    </tr>
  </table>
</div>

<h2>Letzte Anlässe</h2>

{% assign latest_posts = site.posts | sort: 'date' | reverse %}
{% for post in latest_posts limit: 2 %}
{% assign post_image = post.image | default: '/assets/images/mrlebies-red-backs-1201550_1920.jpg' %}
<article class="event-teaser card mb-4">
  <div class="row g-0 align-items-stretch">
    <div class="col-md-4">
      <img class="event-teaser__image" src="{{ post_image | relative_url }}" alt="{{ post.title }}" />
    </div>
    <div class="col-md-8">
      <div class="card-body p-4">
        <span class="event-teaser__date"><time datetime="{{ post.date | date_to_xmlschema }}">{{ post.date | date: "%d. %B %Y" }}</time></span>
        <h3 class="h4 mt-3 mb-2"><a href="{{ post.url | relative_url }}" class="text-decoration-none text-dark">{{ post.title }}</a></h3>
        <p class="text-muted mb-3">{{ post.excerpt | strip_html | truncate: 180 }}</p>
        <a href="{{ post.url | relative_url }}" class="btn event-teaser__link">Mehr lesen</a>
      </div>
    </div>
  </div>
</article>
{% endfor %}
