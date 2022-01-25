<template>
<!-- Beautifull accessible cross module login component -->

  <v-app>
    <v-app-bar
      app
      color="primary"
      dark
    >    </v-app-bar>

    <v-content>
      <v-card width="500" class="mx-auto mt-5">
        <v-card-title>
          <h1 class="display-1">Login</h1>
        </v-card-title>
        <v-card-text > 
          <v-form>
          <v-text-field prepend-icon="mdi-account" type="text" label="Username"></v-text-field>
          <v-text-field prepend-icon="mdi-lock" :type="showPassword ? 'text': 'password'" label="Password" :append-icon="showPassword ? 'mdi-eye':'mdi-eye-off'" @click:append="showPassword= !showPassword"></v-text-field>
</v-form>
        </v-card-text>
        <v-divider></v-divider>
        <v-card-actions>
          <v-btn color="success">Register</v-btn>
        <v-spacer></v-spacer>
          <v-btn color="primary">Login</v-btn>
        </v-card-actions>
      </v-card>
    </v-content>

    <v-main>
  
    </v-main>
  </v-app>
</template>

<script>


export default {
  name: 'App',

  components: {
  
  },

  data: () => ({
    showPassword:false
  }),
};
</script>
