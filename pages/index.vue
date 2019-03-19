<template>
  <div>
    <headerComp/>
    <navBar :config="config"/>
    <drawer :config="config"/>
  </div>
</template>

<script>
import headerComp from "~/components/navBar/headerComp.vue";
import navBar from "~/components/navBar/navBar.vue";
import drawer from "~/components/navBar/drawer.vue";
// import editorComp from "~/components/editorComp.vue";
export default {
  data() {
    return {
      config: {
        drawer: false
      }
    };
  },
  components: {
    headerComp,
    navBar,
    drawer
    // editorComp
  }
};
</script>
