<template>
  <v-card class="ma-auto" style="width: 500px">
    <v-sheet class="pa-4 primary lighten-2">
      <v-text-field
        v-model="search"
        label="Enter text here to search .."
        dark
        flat
        solo-inverted
        hide-details
        clearable
        clear-icon="mdi-close-circle-outline"
      ></v-text-field>
    </v-sheet>
    <v-card-text>
      <v-treeview :items="items" :search="search" :open.sync="open">
      </v-treeview>
    </v-card-text>
  </v-card>
</template>
<script>
import myJson from '../components/data.json';
export default {
  data: () => ({
    items: myJson,
    open: [],
    search: null
  })
};
</script>
