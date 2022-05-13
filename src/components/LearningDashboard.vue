<template>
  <div class="learning-dashboard">
    <div class="list-vocabulary">
      <h1>N4語彙一覧</h1>
      <table class="table-list">
        <TableHeader></TableHeader>
        <TableBody
          :detailData="selectDetail"
          @selectedWord="selectWord"
        ></TableBody>
      </table>
    </div>
  </div>
</template>

<script>
import TableHeader from "./TableHeader.vue";
import TableBody from "./TableBody.vue";

export default {
  components: {
    TableHeader,
    TableBody,
  },
  data() {
    return {
      selectDetail: {},
    };
  },
  methods: {
    selectWord(kanji) {
      console.log(kanji);
      this.selectDetail = kanji;
    },
  },
};
</script>

<style lang="css" scoped>
.table-list {
  width: 100%;
}
.table-header {
  font-weight: bold;
  color: blueviolet;
}
</style>
