<template>
  <v-container class="fill-height" fluid>
    <v-row align="center" justify="center">
      <v-col cols="12" sm="8" md="4">
        <v-card class="elevation-12">
          <v-toolbar color="primary" dark flat>
            <v-toolbar-title>Login form</v-toolbar-title>
          </v-toolbar>
          <v-card-text>
            <v-form>
              <v-text-field label="Username" name="login" prepend-icon="mdi-account" type="text"/>
              <v-text-field
                :type="showPassword ? 'text': 'password'"
                label="Password"
                name="password"
                prepend-icon="mdi-lock"
                :append-icon="showPassword ? 'mdi-eye' : 'mdi-eye-off'"
                @click:append="showPassword = !showPassword"
              />
            </v-form>
          </v-card-text>
          <v-card-actions>
            <v-btn color="success">Register</v-btn>
            <v-spacer></v-spacer>
            <v-btn color="primary">Login</v-btn>
          </v-card-actions>
        </v-card>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  name: 'Home',

  data: () => ({
    showPassword: false
  })
}
</script>
