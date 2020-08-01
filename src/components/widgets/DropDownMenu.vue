<template>
  <v-menu top :offset-x="true">
    <template v-slot:activator="{ on, attrs }">
      <v-icon v-bind="attrs" v-on="on">mdi-dots-vertical</v-icon>
    </template>

    <v-list>
      <v-list-item v-for="(item, index) in menuItems" :key="index">
        <v-list-item-title>{{ item.name }}</v-list-item-title>
      </v-list-item>
    </v-list>
  </v-menu>
</template>

<script>
export default {
  props: {
    menuItems: {
      type: Array,
      default: () => []
    }
  }
};
</script>