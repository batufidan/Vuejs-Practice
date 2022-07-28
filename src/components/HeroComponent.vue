<template>
  <v-container class="pt-15">
    <v-row >
        <v-main-left class="v-row">
            <v-col lg="6">
                <h2 class="intro-text">Welcome to our Vuetify App</h2>
            <v-col lg="12">
                <p class="description">Lorem ipsum dolor sit amet, consectetur adipisicing elit. Doloribus cum omnis nam aperiam sint, ipsum placeat consequuntur. Velit animi non, in temporibus odio, laudantium numquam ducimus quisquam et nemo aliquam!
                </p>
                <v-btn color="success" class="white--text mr-10" rounded>Get Started</v-btn>
                <v-btn color="indigo" class="white--text" rounded>
                    <v-icon>mdi-play-circle</v-icon> Watch Video
                </v-btn>
            </v-col>
            </v-col>
            <v-col lg="6">
                <img width="100%" src="./../assets/hero-img.png" alt="">
            </v-col>
        </v-main-left>
    </v-row>
  </v-container>
</template>

<script>
export default {

}
</script>

<style scoped>
    .v-row {
        display: flex;
    }
    h2.intro-text {
        font-size: 60px;
        font-weight: bold;
        font-family: cursive;
        color: #444;
    }
    p.description {
    font-size: 19px;
    font-family: cursive;
    color: #444444ba;
    margin: 32px 0px;
    }

</style>