<template>
  <div class="container">
    <div class="row">
      <div class="col-md-12">
        <app-header></app-header>
      </div>
    </div>
    <router-view></router-view>
  </div>
</template>

<script>
import Header from './components/Header.vue';
export default {
  components: {
    appHeader: Header
  },
  created() {
    this.$store.dispatch('initStocks');
  }
}
</script>

<style>
  body {
    padding: 30px;
  }
</style>
