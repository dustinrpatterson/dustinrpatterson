<template>
  <v-container
    fill-height
    fluid>
    <v-slide-y-transition mode="out-in">
      <v-layout
        row
        wrap
        class="portfolio pa-3">
        <v-flex
          v-for="(project, index) in projects"
          :key="index"
          xs12
          sm6
          md4
          pa-4>
          <v-card class="portfolio-card">
            <a
              :href="project.url"
              target="_blank"
              style="overflow:hidden;">
              <v-card-media
                :src="project.logo"
                height="200px" /></a>
            <v-card-title primary-title>
              <div>
                <a
                  :href="project.url"
                  target="_blank">
                  <h3 class="headline mb-0">{{ project.name }}</h3>
                </a>
                <div class="tech">
                  <strong>TECH: {{ project.techStack }} </strong>
                </div>
                <div>{{ project.description }}</div>
              </div>
            </v-card-title>
          </v-card>
        </v-flex>
      </v-layout>
    </v-slide-y-transition>
  </v-container>
</template>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
.container {
  background-size: cover;
  background-position: center;
  background-image: url("../assets/keyboard.jpg");
  padding: 0;
}
.portfolio {
  background-size: cover;
  // background: linear-gradient(217deg,rgba(255, 0, 0, 0.8),rgba(255, 0, 0, 0) 70.71%),
  // linear-gradient(127deg, rgba(0, 255, 0, 0.8), rgba(0, 255, 0, 0) 70.71%),
  // linear-gradient(336deg, rgba(0, 0, 255, 0.8), rgba(0, 0, 255, 0) 70.71%);
  background: radial-gradient(
    rgba(45, 45, 45, 0.6) 20%,
    rgba(45, 45, 45, 0.9) 80%
  );
  height: 100%;
  color: white;
}
.portfolio-card {
  overflow: hidden;
}
  .card__media {
    transition: all .2s ease-in-out;
    &:hover{
      transform: scale(1.1);
    }
  }

</style>

<script>
export default {
  name: 'Portfolio',
  data () {
    return {
      projects: [
        {
          name: 'Eddie Bauer',
          url: 'https://www.eddiebauer.com/',
          logo: 'static/EddieBauer.jpg',
          description:
            'Built custom AEM (Adobe Experience Manager) components for eddiebauer.com. Components were built to allow flexibility in authoring while being intuitive for the creative team. Wrote technical documentation and authoring instructions for each component. Provided training to client.',
          techStack: 'HTML, CSS, AEM, JavaScript, jQuery, Sightly'
        },
        {
          name: 'Eddie Bauer Wellness Tool ',
          url: 'https://wellness.eddiebauer.com',
          logo: 'static/wellness.jpg',
          description:
            'Created a web application for Eddie Bauer employees to track their health and wellness for annual incentives from HR. Tool was built to be responsive and offered cross-browser support. Tool was built in AEM to allow HR the flexibility to update wellness steps annually.',
          techStack: 'HTML, Less, AEM, JavaScript, jQuery, Sightly'
        },
        {
          name: 'Revance TV ',
          url: 'http://revancetv.com/',
          logo: 'static/revance.jpg',
          description:
            'Coded AppleTV, Roku, Amazon Fire, and web applications that allowed health care professionals to watch industry-related media. Assisted in front-end development, cloud function API creation, and TV application development. Adapted to new technologies and business requirements.',
          techStack: 'HTML, Sass, Vue JS, Azure Cloud Functions'
        },
        {
          name: 'Quorum Business Solutions ',
          url: 'https://www.quorumsoftware.com/',
          logo: 'static/quorum.jpg',
          description:
            'Redesigned quourmsoftware.com to a mobile friendly, responsive website. Worked collaboratively with offsite developers. Development was done in an agile manner and required outside-the-box thinking to satisfy unique and evolving design requirements.',
          techStack: 'HTML, Sass, FlexBox, Umbraco, JavaScript'
        },
        {
          name: 'Toyo Tires ',
          url: 'https://www.toyotires.com/',
          logo: 'static/toyo.jpg',
          description:
            'Supported updates to Umbraco components for toyo.com related to site enhancements and bug fixes. Assisted with new feature requests associated with new marketing campaigns. Assisted with content edits/updates within CMS.',
          techStack: 'HTML, Sass, Angular JS, Umbraco'
        },
        {
          name:
            'Athene Holding, T-Mobile, GLG, Microsoft, Avaya, Ray Kurzweil ',
          url: 'https://www.glg.com/',
          logo: 'static/glg.jpg',
          description:
            'Assisted as needed to ensure deliverables were completed on-time, defect-free, and exceeding client expectations. Development required team collaboration and clear communication to achieve goals.',
          techStack: 'HTML, CSS, HTML email, etc...'
        }
      ]
    }
  }
}
</script>
