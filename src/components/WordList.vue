<template>
  <table class="tbl-list-word">
    <thead>
      <th>STT</th>
      <th>Kanji</th>
    </thead>
    <tbody>
      <tr v-for="(word, index) in wordData" :key="word.id">
        <td width="50%!important">{{ index + 1 }}</td>
        <td>
          <a @click="selectWord(word)" :class="{ 'click-word': isSelected }">
            {{ word.kanji.first }}{{ word.kanji.middle }}{{ word.kanji.last }}
          </a>
        </td>
      </tr>
    </tbody>
  </table>
</template>

<script>
import data from "./data.json";
export default {
  data() {
    return {
      wordData: data,
      isSelected: false,
    };
  },
  //   methods: {
  //     selectWord(word) {
  //       word.isSelected = !word.isSelected;
  //       word.isSelected ? (this.isSelected = true) : (this.isSelected = false);
  //       this.$emit("selectedWord", word);
  //     },
  //   },
};
</script>

<style lang="css" scoped>
.tbl-list-word {
  width: 100%;
}
.click-word {
  color: darkred;
  font-style: italic;
}
</style>

