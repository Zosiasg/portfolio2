<template>
  <v-col cols="12" sm="12" class="px-16" id="contact">
    <v-row>
      <v-col cols="12" sm="4">
        <div class="child">
          <h1>Contact info.</h1>
          <v-btn
            icon="fas fa-map-marker-alt"
            color=""
            class="mt-10"
            variant="outlined"
          ></v-btn>
          <br />
          <span class="text-caption">Gdańsk, Poland </span>
          <br />
          <v-btn
            icon="fas fa-phone-alt"
            color=""
            class="mt-10"
            variant="outlined"
          ></v-btn>
          <br />
          <span class="text-caption">736-482-937 </span> <br />
          <span class="text-caption">938-472-635 </span> <br />
          <v-btn
            icon="fas fa-envelope"
            color=""
            class="mt-10"
            variant="outlined"
          ></v-btn>
          <br />
          <span class="text-caption">zofiaassg@gmail.com </span> <br />
          <span class="text-caption">alena.mi@gmail.com </span> <br />
        </div>
      </v-col>
      <v-col cols="12" sm="8">
        <h1 class="mt-8">Send your message</h1>
        <v-divider></v-divider>
        <span class="text-caption"
          >If you need a website designed or developed, feel free to send us a message!
          We would be happy to discuss your project and provide you with a quote. Contact us today to get started!</span
        >
        <form action="https://getform.io/f/d15a9529-660c-4b7e-a281-d9dda634f056" method="POST" enctype="multipart/form-data">
          <v-row class="mt-10">
            <v-col cols="12" sm="6">
              <v-text-field
                type="text"
                label="Name"
                persistent-hint
                variant="outlined"
                name="name"
              ></v-text-field>
            </v-col>
            <v-col cols="12" sm="6">
              <v-text-field
                type="email"
                label="Email"
                persistent-hint
                variant="outlined"
                name="email"
              ></v-text-field>
            </v-col>
          </v-row>
          <v-textarea
            label="Message"
            persistent-hint
            variant="outlined"
            name="message"
          ></v-textarea>
          <div class="button-container">
            <v-btn color="#2288f5" class="mr-2" type="submit">Submit Now</v-btn>
            <v-btn color="red" dark @click="goBack">Go back</v-btn>
        </div>
        </form>
      </v-col>
    </v-row>
  </v-col>

</template>

<script>
export default {
  name: "ContactView",
  methods: {
    goBack() {
      this.$router.go(-1); // Go back to the previous page
      location.reload;
    }
  },
};
</script>
