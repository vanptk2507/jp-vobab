<template>
  <tbody>
    <tr v-for="(word, index) in wordData" :key="word.id">
      <td>{{ index + 1 }}</td>
      <td>
        <a
          @click="selectWord(word)"
          :class="{ 'click-word': wordSelected === word }"
        >
          {{ word.kanji.first }}{{ word.kanji.middle }}{{ word.kanji.last }}
        </a>
      </td>
      <td v-show="wordSelected === word">
        {{ word.kanetsu.first }} {{ word.kanetsu.middle }}
        {{ word.kanetsu.last }}
      </td>
      <td v-show="wordSelected === word">{{ word.furigana }}</td>
      <td v-show="wordSelected === word">{{ word.meanings }}</td>
    </tr>
  </tbody>
</template>

<script>
import data from "./data.json";
export default {
  props: {
    detailData: {
      type: Object,
      isSelected: false,
    },
  },
  data() {
    return {
      wordData: data,
      wordSelected: "",
    };
  },
  methods: {
    selectWord(word) {
      word.isSelected = true;
      this.wordSelected = word;
      this.$emit("selectedWord", word);
    },
  },
};
</script>
