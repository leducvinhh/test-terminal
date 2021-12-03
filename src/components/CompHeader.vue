<template>
  <div id="app">
    <h3 @click="handleClick">{{ number }}</h3>
    <button @click="number += 1">Change title</button>
  </div>
</template>

<script>
export default {
  name: 'comp-header',
  data() {
    return {
      number: 1
    }
  },
  methods: {
    handleClick() {
      this.$destroy()
    }
  },
  beforeCreate() {
    console.log('before create');
  },
  create() {
    console.log('create!');
  },
  beforeMount() {
    console.log('before mount!');
  },
  mounted() {
    console.log('mounted!');
  },
  beforeUpdate() {
    console.log('before update!');
  },
  updated() {
    console.log('updated!');
  },
  beforeDestroy() {
    console.log('before destroy');
  },
  destroyed() {
    console.log('destroyed');
  }

}
</script>

<style>

</style>