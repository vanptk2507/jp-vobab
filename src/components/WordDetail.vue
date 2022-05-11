<template>
  <div
    class="word-detail-container"
    v-if="Object.keys(detailData).length !== 0"
  >
    <div class="kanetsu">
      Âm Hán Việt: {{ detailData.kanetsu.first }}
      {{ detailData.kanetsu.middle }} {{ detailData.kanetsu.last }}
    </div>
    <div class="furigana">Cách đọc furigana: {{ detailData.furigana }}</div>
    <div class="meaning">Ý nghĩa: {{ detailData.meanings }}</div>
  </div>
</template>

<script>
export default {
  props: {
    detailData: {
      type: Object,
      isSelected: false,
    },
  },
};
</script>

<style lang="css" scoped>
</style>
