<template>
  <v-container
    fill-height
    fluid>
    <v-slide-y-transition mode="out-in">
      <v-layout
        row
        wrap>
        <v-flex
          xs12
          d-flex
          align-center
          justify-center
          class="home pa-3">
          <div class="home-text">
            <h1 class="text-xs-center">Education</h1>

          </div>

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
  background-image: url("../assets/mountains.jpg");
  -webkit-filter: grayscale(1);
  filter: grayscale(1);
  padding: 0;
}
.home {
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
</style>
