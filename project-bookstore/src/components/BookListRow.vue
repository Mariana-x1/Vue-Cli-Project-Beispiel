<template>
  <tr class="table-item__table-row">
    <td>{{ title }}</td>
    <td>{{ isbn }}</td>
    <td>
      <BaseButton
        :text="buttonText"
        variant="secondary"
        @btn-clicked="toggleBookmark"
      />
    </td>
  </tr>
</template>

<script>
import BaseButton from "@/components/BaseButton.vue";

export default {
  props: {
    title: String,
    isbn: String,
    isBookmarked: Boolean,
  },
  components: {
    BaseButton,
  },
  computed: {
    buttonText() {
      return this.isBookmarked ? "Remove Bookmark" : "Add Bookmark";
    },
  },
  methods: {
    toggleBookmark() {
      this.$emit("bookmark-clicked", this.isbn);
    },
  },
};
</script>

<style scoped>
.table-item__table td {
  padding: 12px 15px;
}
</style>
