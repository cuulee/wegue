<template>

  <div class="">

    <v-btn icon @click="toggleUi">
      <v-icon medium>{{icon}}</v-icon>
      {{text}}
    </v-btn>

    <wgu-measuretool-win
      ref="measurewin"
      :icon="icon"
      :left="left"
      :top="top"
    />

  </div>

</template>


<script>

import MeasureWin from './MeasureWin'

export default {
  name: 'wgu-toggle-measurewin-button',
  components: {
    'wgu-measuretool-win': MeasureWin
  },
  data: function () {
    return {
      show: false,
      icon: 'photo_size_select_small',
      text: '',
      left: '100px',
      top: '200px'
    }
  },
  methods: {
    toggleUi () {
      // TODO move to a father class
      this.$refs.measurewin.show = !this.$refs.measurewin.show;
      this.show = this.$refs.measurewin.show;
    }
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style>
</style>
