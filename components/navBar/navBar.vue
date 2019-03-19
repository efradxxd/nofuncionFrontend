<template>
  <v-toolbar class="style_toolbar">
    <v-toolbar-items
      class="hidden-sm-and-down"
      style="padding-right: 2%; margin: auto;"
      id="items-toolbar"
    >
      <v-btn
        v-for="item in toolbar_options"
        :key="item.title"
        :to="{name: 'category-category', params: { category: item.title} }"
        flat
        class="justify-center"
      >
        {{ item.title }}
        <v-icon size="24px">{{item.icon}}</v-icon>
      </v-btn>
    </v-toolbar-items>
    <v-menu class="hidden-md-and-up">
      <v-toolbar-side-icon slot="activator" @click="config.drawer = true"></v-toolbar-side-icon>
    </v-menu>
  </v-toolbar>
</template>

<script>
import { mapMutations, mapState } from "vuex";

export default {
  props: ["config"],
  data() {
    return {
      title: "New Horizon",
      responsive: false,
      responsiveInput: false,
      toolbar_options: [
        { title: "Upload Note", icon: "create" },
        { title: "Home", icon: "home" }
      ]
    };
  }
};
</script>

<style>
.style_toolbar {
  box-shadow: inherit;
  background-color: inherit;
  border-top: 2px solid #000;
  border-bottom: 2px solid #000;
}
.theme--light.v-toolbar {
  background-color: inherit;
}
#items-toolbar {
  padding-left: 10px;
}
</style>
