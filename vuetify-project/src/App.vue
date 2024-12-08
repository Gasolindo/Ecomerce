<template>
  <v-app>
    <v-card width="400" class="mx-auto mt-10">
      <v-card-title>
        <h1 align="center" class="display-1">Login</h1>
      </v-card-title>
      <v-card-text>
        <v-form>
          <v-text-field width="330"
            label="Matricula"
            prepend-icon="mdi-account-circle"
          />
          <v-text-field
          
            v-model="password"
            :type="showPassword ? 'text' : 'password'"
            label="Senha"
            prepend-icon="mdi-lock"
            :append-icon="showPassword ? 'mdi-eye' : 'mdi-eye-off'"
            @click:append="togglePasswordVisibility"
          />
        </v-form>
      </v-card-text>
      <v-card-actions>
        <v-row justify="center">
          <v-btn color="success">Entrar</v-btn>
        </v-row>
      </v-card-actions>
    </v-card>
  </v-app>
</template>

<script>
  export default {
    data() {
      return {
        password: '',
        showPassword: false,
      };
    },
    methods: {
      togglePasswordVisibility() {
        this.showPassword = !this.showPassword;
      },
    },
  };
</script>
