<template>
  <v-sheet
    width="400"
    height="350"
    elevation="4"
    style="margin-top: 200px"
    class="mx-auto"
  >
    <h4 class="text-h4 font-weight-bold mt-6 text-center">Login</h4>
    <v-form fast-fail @submit.prevent class="pa-8">
      <v-text-field v-model="username" label="Username"></v-text-field>

      <v-text-field
        v-model="password"
        label="Password"
        type="password"
      ></v-text-field>
      <v-divider class="mb-4"></v-divider>
      <div class="text-end" style="display: flex; margin-top: 40px; gap: 10px">
        <v-btn class="text-none" color="success" variant="flat" width="90">
          Submit
        </v-btn>

        <v-btn class="text-none" color="primary" variant="flat" width="90">
          Clear
        </v-btn>
      </div>
    </v-form>
  </v-sheet>
</template>
    <script>
export default {
  data: () => ({
    username: "",

    lastName: "123",
    lastNameRules: [
      (value) => {
        if (/[^0-9]/.test(value)) return true;

        return "Last name can not contain digits.";
      },
    ],
  }),
};
</script>

<style>
</style>