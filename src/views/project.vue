<template>
    <div>
        <main id="project">

            <div class="intro one-third">
                <particles></particles>
                <div class="overlay">
                    <div class="container">
                        <div class="flex flex-center">
                            <span class="intro-text">
                                <h3 class=""><span class="icon icon-window-application-7"></span></h3>
                                <h3>{{ project.name }}</h3>
                            </span>
                        </div>
                    </div>
                </div>
            </div>
            

            <div class="section project-content">
                <div class="container container--small">
            
                    <div class="project-logo flex flex-center">
                        <img :src="project.img" alt="">
                    </div>
            
                    <h3 class="project-title">{{ project.client }}
                        <a class="link" v-if="project.address" v-bind:href="project.address" target="_blank"><small class="text-muted">{{ project.type }}</small></a>
                        <small class="text-muted" v-else>{{ project.type }}</small>
                    </h3>

                    <p class="project-text" v-html="project.text"></p>

                    <div v-if="project.tasks" class="project-tasks">
                        <h2>Taken</h2>
                        <ul>
                            <li v-for="task in project.tasks" :key="task">{{ task }}</li>
                        </ul>
                    </div>

                    <div>
                        <div class="badge badge-primary" v-for="technique in project.techniques" :key="technique">{{ technique }}</div>
                    </div>

                </div>
            </div>
            <div v-if="project.screenshots" class="section bg-gray-lightest">
                <div class="container">
                    <div class="screenshots">
                        <project-image v-for="screenshot in project.screenshots" :file="screenshot.file" :direction="screenshot.direction" :url="screenshot.url" :key="screenshot.file"></project-image>
                    </div>
                </div>
            </div>

        </main>
    </div>
</template>

<script>
import ProjectsResource from "../services/projectsResource.js";
const restProjectsResource = new ProjectsResource();

let particles = require("particles.js");

export default {
  name: "project",
  mounted: () => {
    window.scrollTo(0, 0);
  },
  created() {
    console.log('here i was');
    console.log('i left a line');
    console.log('just joking');
  },
  data() {
    return {
      project: restProjectsResource.getProject(this.$route.params.name)
    };
  },
  computed: {}
};
</script>
