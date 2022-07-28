<template>
    <v-footer
    padless
  >
  <v-col lg="12">
    <v-row justify="center">
        <v-col lg="4" class="text-center">
            <v-toolbar-title>VueJs Practice</v-toolbar-title>
            <v-card-text>
                <v-btn
                    v-for="icon in icons"
                    :key="icon"
                    class="mx-4 black--text"
                    icon
                    >
                    <v-icon size="24px">
                        {{ icon }}
                    </v-icon>
                </v-btn>
            </v-card-text>
            <v-subheader>Lorem ipsum dolor sit amet consectetur adipisicing elit. Rem dolorum omnis nostrum suscipit! Laborum in voluptatibus hic ratione laboriosam vel.

            </v-subheader>
            <v-form class="mt-4">
                <v-text-field label="Email" outlined dense />
                <v-btn rounded color="success">Subscribe us</v-btn>
            </v-form>
        </v-col>

    </v-row>

            <div class="mt-10 d-flex align-items">
            <v-subheader>® Copyright VueJS Practice. All Rights Reserved         {{ new Date().getFullYear() }} — <strong>Vuetify</strong> </v-subheader>
            <v-spacer />
            <strong>Designed by Batuhan Fidan</strong>
        </div>
  </v-col>
    
  </v-footer>
</template>

<script>
export default {
    // eslint-disable-next-line vue/multi-word-component-names
    name: "Footer ",
    data () {
        return{
        icons: [
            'mdi-facebook',
            'mdi-twitter',
            'mdi-linkedin',
            'mdi-instagram',
        ],
        }
    }

}
</script>

<style>

</style>