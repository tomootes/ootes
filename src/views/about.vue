<template>

  <div>

    <main id="about">

      <div class="intro one-third">
        <particles></particles>
        <div class="overlay">
          <div class="container">
            <div class="flex flex-center">
              <span class="intro-text">
                <h3 class=""><span class="icon icon-id-card-2"></span></h3>
                <h3>Over</h3>
              </span>
            </div>
          </div>
        </div>
      </div>

      <div class="section">
        <div class="container">
          <div class="flex flex-space-between content">
            <div class="col-8 picture">
              <img
                src="img/swu.jpg"
                class="img-fluid bg-primary-light"
                alt="Tom Ootes"
              >
            </div>
            <div class="col-4 company-info">
              <!-- <h2>Gegevens</h2> -->
              <p><a
                  href="email:tom@ootes.io"
                  target="_blank"
                  class="link"
                >tom@ootes.io</a></p>
              <p><a
                  href="tel:+31623447230"
                  class="link"
                >+31623447230</a></p>
              <!-- <p>BTW: NL209059643B01</p> -->
              <p><b>KVK</b> 59479817</p>
              <p><b>IBAN</b> NL06ASNB0708907997</p>
            </div>

            <div class="story">
              <h1>Sociale uitvinder, web developer</h1>
              <!-- <img src="img/pixel-me-nobg.png" class="story__photo" alt="Tom"> -->
              <p>Hoi, ik ben Tom, aangenaam. Ootes Web is mijn bureau. Na anderhalf jaar als programmeur in vaste dienst te hebben gewerkt besloot ik te vertrekken. Ik nam de trein van Rusland naar Mongolië en daarna China. Na een aantal omzwervingen kwam ik weer terug in Nederland. Toen mijn reis er op zat besloot ik het avontuurlijke element in mijn dagelijkse leven te bakken en voor mezelf te beginnen. Sindsdien heb ik met een hoop plezier als full-stack en front-end programmeur aan verschillende projecten gewerkt. </p>
              <p>Ik ben sterk in de volgende facetten van webprojecten:</p>
              <ul>
                <li>Modulair opzetten van styleguides mbv components</li>
                <li>Code-technisch overzicht, technisch advies</li>
                <li>Bewaken van esthetiek en gebruiksvriendelijkheid</li>
              </ul>
              <p>Verder ben ik erg geïnteresseerd in het meebouwen aan een internet waarin we <b>machtsblokken oplossen</b> door het bouwen van <b>open software</b> op basis van publieke waarden.</p>
              <p>De mogelijkheden bespreken? Ik ben altijd in voor een bakkie koffie.</p>
            </div>
          </div>
        </div>
      </div>
    </main>

  </div>
</template>

    <script>
let particles = require("particles.js");

export default {
  name: "about",
  data() {
    return {
      projects: {},
    };
  },
};
</script>
