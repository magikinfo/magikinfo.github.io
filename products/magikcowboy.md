---
layout: page
title: Magik Cowboy
permalink: /products/magikcowboy
---
{% assign magikcowboy_schedule_img = '/assets/images/magikcowboy/schedule.png' | relative_url %}
{% assign magikcowboy_detail_img = '/assets/images/magikcowboy/event-detail.png' | relative_url %}

Magik Cowboy is a [Team Cowboy](https://teamcowboy.com) client for iOS (iPhone and iPad). It is designed so you can easily look at your sports events schedule, RSVP, and see who is attending.

An Android version is still in development and will be coming soon.

- **Schedule** — See your teams’ upcoming events in one scroll: date and time, opponent, location, and team notes—with color-coded RSVP counts so you can see who is in at a glance.
- **Event detail** — Open an event to set your status (yes, maybe, or no), add a comment, and see who is **Playing** or cannot make it.

<div class="magikcowboy-screenshots" markdown="0">
  <button type="button" class="magikcowboy-thumb" aria-label="View schedule screenshot full size">
    <img src="{{ magikcowboy_schedule_img }}" alt="Magik Cowboy schedule: list of upcoming events with locations, RSVP counts, and details" loading="lazy" decoding="async" />
  </button>
  <button type="button" class="magikcowboy-thumb" aria-label="View event detail screenshot full size">
    <img src="{{ magikcowboy_detail_img }}" alt="Magik Cowboy event detail: RSVP controls, comment, and attendee lists" loading="lazy" decoding="async" />
  </button>
</div>

<dialog class="magikcowboy-lightbox" id="magikcowboy-lightbox" aria-modal="true" aria-label="Screenshot preview">
  <button type="button" class="magikcowboy-lightbox-close" aria-label="Close">&times;</button>
  <img class="magikcowboy-lightbox-img" src="" alt="" />
</dialog>

<script>
(function () {
  var dialog = document.getElementById('magikcowboy-lightbox');
  if (!dialog || !dialog.showModal) return;
  var lightboxImg = dialog.querySelector('.magikcowboy-lightbox-img');
  var closeBtn = dialog.querySelector('.magikcowboy-lightbox-close');
  document.querySelectorAll('.magikcowboy-thumb').forEach(function (btn) {
    btn.addEventListener('click', function () {
      var thumb = btn.querySelector('img');
      if (!thumb) return;
      lightboxImg.src = thumb.currentSrc || thumb.src;
      lightboxImg.alt = thumb.alt || '';
      dialog.showModal();
      closeBtn.focus();
    });
  });
  function closeLightbox() {
    dialog.close();
  }
  dialog.addEventListener('close', function () {
    lightboxImg.removeAttribute('src');
    lightboxImg.alt = '';
  });
  closeBtn.addEventListener('click', closeLightbox);
  dialog.addEventListener('click', function (e) {
    if (e.target === dialog) closeLightbox();
  });
})();
</script>

{% if site.magik_cowboy.app_store_url != "" %}
<p class="magikcowboy-app-store-badge">
  <a href="{{ site.magik_cowboy.app_store_url }}" target="_blank" rel="noopener noreferrer">
    <img src="{{ site.magik_cowboy.app_store_badge_image_url }}" alt="Download on the App Store" width="246" height="82" loading="lazy" decoding="async" />
  </a>
</p>
{% else %}
Coming soon on the App Store.
{% endif %}

### Support

For help with Magik Cowboy, email [support@magikinfo.com](mailto:support@magikinfo.com?subject=Magik%20Cowboy%20support).


### Legal

- [Privacy policy]({{ '/products/magikcowboy/privacy' | relative_url }})
- [Terms of use]({{ '/products/magikcowboy/terms' | relative_url }})

#### Logos (Vecteezy)

Certain logos used for Magik Cowboy on this site are licensed from [Vecteezy](https://www.vecteezy.com/) and Brian Goff.

For full rules, see [Vecteezy’s licensing section](https://www.vecteezy.com/licensing) or contact Vecteezy support. The [Vecteezy Terms of Use](https://www.vecteezy.com/terms) supersede any summary on this page.
