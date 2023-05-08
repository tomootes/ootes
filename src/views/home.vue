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

    <location></location>

  </div>
</template>
