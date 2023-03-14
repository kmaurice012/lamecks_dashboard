<template>
  <v-card class="main_card">
    <v-dialog transition="dialog-top-transition" class="ma-3" width="400px">
      <template v-slot:activator="{ props }">
        <v-btn color="grey-darken-4 " class="mb-2 mt-2" v-bind="props"
          >Create</v-btn
        >
      </template>
      <template v-slot:default="{ isActive }">
        <v-card>
          <v-toolbar color="grey-darken-3" title="Create Account"></v-toolbar>
          <v-card-text>
            <div class="text-h2 pa-2">
              <v-text-field v-model="username" label="Username"></v-text-field>
              <v-text-field
                v-model="email"
                type="email"
                label="Email"
              ></v-text-field>
              <v-text-field
                v-model="password"
                type="password"
                label="Password"
              ></v-text-field>
              <v-text-field v-model="contact" label="Contact"></v-text-field>
            </div>
          </v-card-text>
          <v-card-actions class="justify-end">
            <v-btn variant="outlined" @click="isActive.value = false"
              >Submit</v-btn
            >

            <v-btn variant="outlined" @click="isActive.value = false"
              >Close</v-btn
            >
          </v-card-actions>
        </v-card>
      </template>
    </v-dialog>

    <v-table theme="dark">
      <thead>
        <tr>
          <th class="text-left">Name</th>
          <th class="text-left">Calories</th>
          <th class="text-left">Action</th>
        </tr>
      </thead>
      <tbody>
        <tr v-for="item in desserts" :key="item.name">
          <td>{{ item.name }}</td>
          <td>{{ item.calories }}</td>
          <td class="d-flex">
            <v-icon color="green-darken-2" icon="mdi-pencil"></v-icon
            ><v-icon color="red-darken-2" icon="mdi-delete"></v-icon>
          </td>
        </tr>
      </tbody>
    </v-table>
  </v-card>
</template>
  <script>
export default {
  data() {
    return {
      username: "",
      email: "",
      password: "",
      contact: "",
      desserts: [
        {
          name: "Frozen Yogurt",
          calories: 159,
        },
        {
          name: "Ice cream sandwich",
          calories: 237,
        },
        {
          name: "Eclair",
          calories: 262,
        },
        {
          name: "Cupcake",
          calories: 305,
        },
        {
          name: "Gingerbread",
          calories: 356,
        },
        {
          name: "Jelly bean",
          calories: 375,
        },
        {
          name: "Lollipop",
          calories: 392,
        },
        {
          name: "Honeycomb",
          calories: 408,
        },
        {
          name: "Donut",
          calories: 452,
        },
        {
          name: "KitKat",
          calories: 518,
        },
      ],
    };
  },
};
</script>
<style scoped>
.main_card {
  margin: 2px;
}
</style>