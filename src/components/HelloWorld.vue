<template>
  <div class="hello">
    <h2>{{ msg }}</h2>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String,
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
h2 {
  padding-top: 3rem;
  font-family: 'Gulim';
  font-size: 1.5rem;
  font-weight: 900;
  color: #515e6d;
}
</style>
