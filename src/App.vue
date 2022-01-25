<template>
  <!-- Beautifull accessible cross module login component -->

  <v-app>
    <v-app-bar app color="primary" dark>
      <v-toolbar-title> Default Dashboard </v-toolbar-title>
      <v-spacer></v-spacer>
      <v-card-actions>
        <v-btn text rounded>Home</v-btn>
        <v-btn text rounded>Login</v-btn>
      </v-card-actions>
    </v-app-bar>
    <v-main>
      <v-card width="500" class="mx-auto mt-5">
        <v-card-title>
          <h1 class="display-1">Login</h1>
        </v-card-title>
        <v-card-text>
          <v-form>
            <v-text-field
              prepend-icon="mdi-account"
              type="text"
              label="Username"
            ></v-text-field>
            <v-text-field
              prepend-icon="mdi-lock"
              :type="showPassword ? 'text' : 'password'"
              label="Password"
              :append-icon="showPassword ? 'mdi-eye' : 'mdi-eye-off'"
              @click:append="showPassword = !showPassword"
            ></v-text-field>
          </v-form>
        </v-card-text>
        <v-divider></v-divider>
        <v-card-actions>
          <v-btn color="success">Register</v-btn>
          <v-spacer></v-spacer>
          <v-btn color="primary">Login</v-btn>
        </v-card-actions>
      </v-card>
    </v-main>

    <!-- <v-footer dark padless>
      <v-card flat tile class="primary lighten-1 white--text text-center">
        <v-card-text>
          <v-btn
            v-for="icon in icons"
            :key="icon"
            class="mx-4 white--text"
            icon
          >
            <v-icon size="24px">
              {{ icon }}
            </v-icon>
          </v-btn>
        </v-card-text>

        <v-card-text class="white--text pt-0">
          iaculis dui sollicitudin. Vestibulum eu ipsum vel diam elementum
          tempor vel ut orci. Orci varius natoque penatibus et magnis dis
          parturient montes, nascetur ridiculus mus.
        </v-card-text>

        <v-divider></v-divider>

        <v-card-text class="white--text">
          {{ new Date().getFullYear() }} — <strong>Vuetify</strong>
        </v-card-text>
      </v-card>
    </v-footer> -->
    <v-footer color="primary lighten-1" padless>
      <v-row justify="center" no-gutters>
        <v-btn
          v-for="link in links"
          :key="link"
          color="white"
          text
          rounded
          class="my-2"
        >
          {{ link }}
        </v-btn>
        <v-col class="primary lighten-2 py-4 text-center white--text" cols="12">
          {{ footerDate }} — <strong>Vuetify</strong>
        </v-col>
      </v-row>
    </v-footer>
  </v-app>
</template>

<script>
export default {
  name: "App",

  components: {},

  data: () => ({
    footerDate: new Date(),

    showPassword: false,
    icons: ["mdi-facebook", "mdi-twitter", "mdi-linkedin", "mdi-instagram"],
    links: ["Home", "About me", "Contact me"],
  }),
};
</script>
