<template>
  <v-container class="header_container">
    <v-layout row wrap>
      <v-flex xs12 md4></v-flex>
      <v-flex xs12 md4>
        <v-img src="https://s3.amazonaws.com/nh-prototype/El+General+Oficial+500x168.png"></v-img>
      </v-flex>
    </v-layout>
    <v-flex xs12 md12 style="text-align: center">
      <p>{{date}}</p>
      <h1>Admin</h1>
    </v-flex>
  </v-container>
</template>

<script>
export default {
  data() {
    return {
      date: "" + this.getFecha() + " " + "Victoria de Durango" + " ,Durango"
    };
  },
  methods: {
    getFecha: function() {
      var p = new Date();
      return (
        "" + p.getDate() + "/" + (p.getMonth() + 1) + "/" + p.getFullYear() + ""
      );
    }
  }
};
</script>

<style>
.container .header_container {
  padding: 0;
}
#info-toolbar {
  box-shadow: inherit;
  background-color: inherit;
}
.theme--light.v-toolbar {
  background-color: inherit;
}
</style>
