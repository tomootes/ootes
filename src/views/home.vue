<script setup>
import Card from '../components/Card.vue'
</script>

<template>
  <div>

    <div class="intro full-height">
      <particles></particles>
      <div class="overlay">
        <div class="container">
          <span class="intro-text">
            <span class="icon icon-greenhouse"></span>
            <h2 class="heading">Web developer met oog voor het grotere plaatje</h2>
            <a href="#/about">
              <button type="button" class="btn btn--white">Samen werken aan het web?</button>
            </a>
          </span>
          <div class="bottom">
            <span class="down">Δ</span>
          </div>

        </div>
      </div>
    </div>

    <div class="section point-section ">
      <div class="container">
        <h2 class="section--heading flex-center">Opdrachtgevers</h2>
        <div class="row cards-holder">
          <Card />
          <!-- <card v-for="project in projects" key="project" :title="project.name" url="project.url" text="project.text" image="project.img"  /> -->
        </div>
        <div class="flex-center gutter-top-small">
          <a v-bind:href="'#/projects/'">
            <button type="button" class="btn btn-outline-secondary ">Alle projecten</button>
          </a>
        </div>
      </div>
    </div>


    <!-- <div class="section">
      <div class="container">
        <h1 class="flex-center">Opdrachtgevers</h1>
        <p class="flex-center">Wij hebben eerder samengewerkt met</p>
        <div class="flex">
          <a v-bind:href="'#/project/' + project.url" class="client" v-for="project in projects" :key="project">
            <img :src= "project.img" />
          </a>
        </div>
        <p class="flex-center">
          <a href="#/projects"><button type="button" class="btn btn-primary">Naar projecten</button></a>
        </p>
      </div>
    </div> -->

    <!-- <div class="section bg-gray-lightest">
      <div class="container">
        <h1 class="flex-center">Techniek</h1>
        <br>
        <div class="row technique">
          <div class="col-3 vertical-center">
            <img src="img/vuejs.png" class="img-fluid" alt="Vue.js">
          </div>
          <div class="col-9">
            <h4 class="heading">Framework</h4>
            <p>Als framework voor onze projecten gebruiken wij Vue. Vue is een lichtgewicht framework dat niet teveel zijn stempel drukt op een project. Dit zorgt ervoor dat je zelf moet blijven nadenken maar ook dat een project niet teveel aan een framework vastzit. Een project kan zo makkelijker worden omgezet naar een ander framework als dit nodig is. Ook de herbruikbaarheid van code is een stuk hoger als het project niet aan een framework vastzit.</p>
          </div>
        </div>
        <br/>
        <div class="row technique">
          <div class="col-3 flex-center">
            <img src="img/sass.svg" class="img-fluid" alt="Sass">
          </div>
          <div class="col-9">
            <h4 class="heading">Styling</h4>
            <p>Voor styling gebruiken wij SASS. Deze techniek zorgt ervoor dat we variabelen kunnen gebruiken en efficiënter kunnen werken. De opmaak is hierdoor consistenter en dit werkt door in de gebruikerservaring en de uitstraling.</p>
          </div>
        </div>
      </div>
    </div> -->

    <location></location>

  </div>
</template>
