<template>
  <div class="form-group input-group">
    <div class="col-sm-2">
      카테고리
    </div>
    <div class="col-sm-2">
      <select name="cno1" class="custom-select" v-on:change="changeCNo1($event)">
        <option v-for="(option, index) in largeCategory"
                v-bind:key="index" v-bind:value="option.value">
          {{ option.text }}
        </option>
      </select>
    </div>
    <div class="col-sm-2">
      <select name="cno2" class="custom-select" v-on:change="changeCNo2($event)">
        <option v-for="(option, index) in middleCategory"
                v-bind:key="index" v-bind:value="option.value">
          {{ option.text }}
        </option>
      </select>
    </div>
    <div class="col-sm-2">
      <select name="cno3" class="custom-select">
        <option v-for="(option, index) in smallCategory"
                v-bind:key="index" v-bind:value="option.value">
          {{ option.text }}
        </option>
      </select>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Category.vue',
  props: ['largeCategory', 'middleCategory', 'smallCategory'],
  methods: {
    changeCNo1(event) {
      if (event.target.value !== '') {
        this.$emit('changeComCNo1', event.target.value);
      }
    },
    changeCNo2(event) {
      this.$emit('changeComCNo2', event.target.value);
    },
  },
};
</script>

<style scoped>

</style>
