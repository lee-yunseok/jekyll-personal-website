---
layout: default
title: "Contact"
permalink: pages/contact/
description: "Contact me if you have question."
---

<form id="fs-frm" name="simple-contact-form" accept-charset="utf-8" action="https://formspree.io/YOUR_EMAIL_ADDRESS" method="post" class="contact">
  <fieldset id="fs-frm-inputs">
    <p><label for="full-name">Full Name</label></p>
    <input type="text" name="name" id="full-name" placeholder="First and Last" required="">
    <p><label for="email-address">Email Address</label></p>
    <input type="email" name="_replyto" id="email-address" placeholder="email@domain.tld" required="">
    <p><label for="message">Message</label></p>
    <textarea rows="5" name="message" id="message" placeholder="Aenean lacinia bibendum nulla sed consectetur. Vivamus sagittis lacus vel augue laoreet rutrum faucibus dolor auctor. Donec ullamcorper nulla non metus auctor fringilla nullam quis risus." required=""></textarea>
    <input type="hidden" name="_subject" id="email-subject" value="Contact Form Submission">
  </fieldset>
  <input type="submit" value="Submit">
</form>
