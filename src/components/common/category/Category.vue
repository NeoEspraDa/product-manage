<template>
  <div class="form-group input-group">
    <div class="col-sm-2">
      카테고리
    </div>
    <div class="col-sm-2">
      <LargeCategory v-bind:largeCategory='largeCategory' @changeCNo1='changeCNo1' />
    </div>
    <div class="col-sm-2">
      <MiddleCategory v-bind:middleCategory='middleCategory' @changeCNo2='changeCNo2' />
    </div>
    <div class="col-sm-2">
      <SmallCategory v-bind:smallCategory='smallCategory' />
    </div>
  </div>
</template>

<script>
import LargeCategory from './LargeCategory.vue';
import MiddleCategory from './MiddleCategory.vue';
import SmallCategory from './SmallCategory.vue';

export default {
  name: 'Category.vue',
  components: {
    LargeCategory,
    MiddleCategory,
    SmallCategory,
  },
  data() {
    return {
      largeCategory: [
        { text: 'One', value: '1' },
        { text: 'Two', value: '2' },
        { text: 'Three', value: '3' },
      ],
      middleCategory: [],
      smallCategory: [],
    };
  },
  methods: {
    changeCNo1(value) {
      this.middleCategory = [];
      this.smallCategory = [];
      if (value === '1') {
        this.middleCategory.push({ text: 'A', value: '1' });
        this.middleCategory.push({ text: 'B', value: '2' });
        this.middleCategory.push({ text: 'C', value: '3' });
      } else if (value === '2') {
        this.middleCategory.push({ text: '가', value: '1' });
        this.middleCategory.push({ text: '나', value: '2' });
        this.middleCategory.push({ text: '다', value: '3' });
      } else if (value === '3') {
        this.middleCategory.push({ text: '#1', value: '1' });
        this.middleCategory.push({ text: '#2', value: '2' });
        this.middleCategory.push({ text: '#3', value: '3' });
      }
    },
    changeCNo2(value) {
      this.smallCategory = [];
      if (value === '1') {
        this.smallCategory.push({ text: '하나', value: '1' });
        this.smallCategory.push({ text: '둘', value: '2' });
        this.smallCategory.push({ text: '셋', value: '3' });
      } else if (value === '2') {
        this.smallCategory.push({ text: '원', value: '1' });
        this.smallCategory.push({ text: '투', value: '2' });
        this.smallCategory.push({ text: '쓰리', value: '3' });
      } else if (value === '3') {
        this.smallCategory.push({ text: '이치', value: '1' });
        this.smallCategory.push({ text: '니', value: '2' });
        this.smallCategory.push({ text: '산', value: '3' });
      }
    },
  },
};
</script>

<style scoped>

</style>
