<template>
  <v-toolbar class="wgu-app-toolbar">
      <v-toolbar-title>{{title}}</v-toolbar-title>
      <v-spacer></v-spacer>

      <!--This <slot> is going to be replaced by the toolbar buttons in the
          app configuration tags (see App.vue) -->
      <v-layout justify-end class="">
        <slot name="wgu-tb-buttons"></slot>
      </v-layout>
    </v-toolbar>
</template>

<script>

export default {
  name: 'wgu-app-header',
  data () {
    return {
      title: this.$appConfig.title
    }
  },
  mounted () {
  }

}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style>

  .wgu-app-toolbar {
    z-index: 1;
    display: block;
  }

</style>
