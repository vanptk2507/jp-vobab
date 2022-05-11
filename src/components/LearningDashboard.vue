<template>
  <div class="learning-dashboard">
    <div class="list-vocabulary">
      <h1>N4語彙一覧</h1>
      <table class="table-list">
        <thead class="table-header">
          <th>Danh sách từ vựng N4</th>
          <th>Thông tin chi tiết từ vựng</th>
        </thead>
        <tbody>
          <td><WordList @selectedWord="selectWord"></WordList></td>
          <td><WordDetail :detailData="selectDetail"></WordDetail></td>
        </tbody>
      </table>
    </div>
  </div>
</template>

<script>
import WordList from "./WordList.vue";
import WordDetail from "./WordDetail.vue";

export default {
  components: {
    WordList,
    WordDetail,
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
