<template>
  <div id="app">
    <vue-editor v-model="content"></vue-editor>
  </div>
</template>

 <script>
import { VueEditor } from "vue2-editor";

export default {
  data() {
    return {
      content: "<h1>Some initial content</h1>"
    };
  },
  components: {
    "vue-editor": VueEditor
  }
};
</script>
