<template>
        <v-container class="my-15">
        <v-row justify="center">
            <v-col lg="12" class="text-center mb-25" >
                <v-subheader class="text-h4 justify-center">Contact</v-subheader>
                <p>Lorem ipsum, dolor sit amet consectetur adipisicing elit. Soluta omnis nulla, voluptatem possimus qui ipsam?</p>
            </v-col>
            <v-col lg="6">
                <iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d12746665.270374443!2d26.184427554396997!3d38.741248117664526!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x14b0155c964f2671%3A0x40d9dbd42a625f2a!2sTurkey!5e0!3m2!1sen!2str!4v1659039670342!5m2!1sen!2str" width="100%" height="100%" style="border:0;" allowfullscreen="" loading="lazy" referrerpolicy="no-referrer-when-downgrade"></iframe>
            </v-col>
            <v-col lg="6">
                  <v-form
    ref="form"
  >
    <v-text-field
      v-model="contactInfo.name"
      :counter="10"
      label="Name"
      required
    ></v-text-field>

    <v-text-field
      v-model="contactInfo.email"
      label="E-mail"
      required
    ></v-text-field>
    <v-textarea label="Message" v-model="contactInfo.message">

    </v-textarea>

    <v-btn
      color="success"
      class="mr-4"
    >
    Send
    </v-btn>
  </v-form>
            </v-col>
        </v-row>
        </v-container>
</template>

<script>
export default {
    // eslint-disable-next-line vue/multi-word-component-names
    name: "Contactus",
    data() {
        return{
            contactInfo:{}
        }
    }

}
</script>

<style>

</style>