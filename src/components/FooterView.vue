<template>
  <v-footer>
      <v-card
        elevation="0"
        rounded="0"
        width="100%"
        class="bg-grey text-center"
      >
        <v-card-text>
          <v-btn
            class="mx-4"
            icon="fa-brands fa-github"
            variant="plain"
            color="white"
            href="https://github.com/"
          ></v-btn>
          <v-btn
            class="mx-4"
            icon="fa-brands fa-facebook"
            variant="plain"
            color="white"
            href="https://facebook.com"
          ></v-btn>
          <v-btn
            class="mx-4"
            icon="fa-brands fa-instagram"
            variant="plain"
            color="white"
            href="https://instagram.com"
          ></v-btn>
          <v-btn
            class="mx-4"
            icon="fa-brands fa-twitter"
            variant="plain"
            color="white"
            href="https://twitter.com"
          ></v-btn>
        </v-card-text>

        <v-card-text class="text-white">
          <strong></strong>
        </v-card-text>
      </v-card>
    </v-footer>
</template>

<script>
export default {

}
</script>

<style>
.v-footer {
  padding: 8px 0 !important;
}
</style>