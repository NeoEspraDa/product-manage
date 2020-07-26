<template>
  <div>
    <div class="text-left p-3">
      카테고리를 컴포넌트로 빼지 않고 직접 구현
    </div>
    <div class="form-group input-group">
      <div class="col-sm-2">
        카테고리
      </div>
      <div class="col-sm-2">
        <!-- @ 대신 v-on으로 처리해봄 -->
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
    <div class="text-left p-3">
      카테고리를 컴포넌트로 빼서 구현
    </div>
    <categoryCom
      v-bind="[
        {largeCategory:largeCategory, middleCategory:middleCategory, smallCategory:smallCategory}
      ]"
      @changeComCNo1='changeComCNo1'
      @changeComCNo2='changeComCNo2'
    />
  </div>
</template>

<script>
import Category from './info/Category.vue';

export default {
  name: 'Info.vue',
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
    changeCNo1(event) {
      this.middleCategory = [];
      this.smallCategory = [];
      if (event.target.value === '1') {
        this.middleCategory.push({ text: 'A', value: '1' });
        this.middleCategory.push({ text: 'B', value: '2' });
        this.middleCategory.push({ text: 'C', value: '3' });
      } else if (event.target.value === '2') {
        this.middleCategory.push({ text: '가', value: '1' });
        this.middleCategory.push({ text: '나', value: '2' });
        this.middleCategory.push({ text: '다', value: '3' });
      } else if (event.target.value === '3') {
        this.middleCategory.push({ text: '#1', value: '1' });
        this.middleCategory.push({ text: '#2', value: '2' });
        this.middleCategory.push({ text: '#3', value: '3' });
      }
    },
    changeCNo2(event) {
      this.smallCategory = [];
      if (event.target.value === '1') {
        this.smallCategory.push({ text: '하나', value: '1' });
        this.smallCategory.push({ text: '둘', value: '2' });
        this.smallCategory.push({ text: '셋', value: '3' });
      } else if (event.target.value === '2') {
        this.smallCategory.push({ text: '원', value: '1' });
        this.smallCategory.push({ text: '투', value: '2' });
        this.smallCategory.push({ text: '쓰리', value: '3' });
      } else if (event.target.value === '3') {
        this.smallCategory.push({ text: '이치', value: '1' });
        this.smallCategory.push({ text: '니', value: '2' });
        this.smallCategory.push({ text: '산', value: '3' });
      }
    },
    changeComCNo1(value) {
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
    changeComCNo2(value) {
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
  components: {
    // 컴포넌트명 지정해서 처리
    categoryCom: Category,
  },
};
</script>

<style scoped>

</style>
