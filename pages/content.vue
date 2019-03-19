<template>
  <div id="app">
    <!-- <VueEditor v-model="content"></VueEditor> -->
    <h1>{{content}}</h1>
  </div>
</template>

 <script>
import VueEditor from "vue2-editor";

export default {
  data() {
    return {
      content: "<h1>Some initial content</h1>"
    };
  },
  components: {
    // VueEditor
  }
};
</script>
