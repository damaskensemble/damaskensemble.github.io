---
layout: page
title: Contact
eyebrow: Get in touch
permalink: /contact/
---

Damask is based in the Netherlands and performs across the Netherlands,
Germany, and beyond. For booking enquiries, commissions, or press
requests, please use the form below or email us directly.

<!--
  GitHub Pages serves static files only — there's no server to receive
  a form POST. The simplest fix is a free form-backend service such as
  Formspree (https://formspree.io): sign up, get an endpoint like
  https://formspree.io/f/xxxxabcd, and drop it into the action=""
  below. Netlify Forms is another option, but requires hosting on
  Netlify rather than GitHub Pages.
-->
<form class="contact-form" action="https://formspree.io/f/YOUR_FORM_ID" method="POST">
  <div>
    <label for="name">Name</label>
    <input type="text" id="name" name="name" required>
  </div>
  <div>
    <label for="email">Email</label>
    <input type="email" id="email" name="email" required>
  </div>
  <div>
    <label for="message">Message</label>
    <textarea id="message" name="message" rows="6" required></textarea>
  </div>
  <button type="submit">Send</button>
</form>

<hr class="rule">

<p>
  <strong>Email:</strong> <a href="mailto:info@damaskquartet.com">info@damaskquartet.com</a><br>
  <strong>Based in:</strong> The Hague, the Netherlands
</p>

<p>
  <a href="https://www.facebook.com/dmskensemble/" target="_blank" rel="noopener">Follow on Facebook &rarr;</a>
</p>
