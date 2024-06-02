<template>
  <div class="tabs">
    <ul class="tabs__heeader">
      <li
        v-for="title in tabTitles"
        :key="title"
        :class="{ selected: title == selectedTitle }"
        @click="selectedTitle = title"
      >
        {{ title }}
      </li>
    </ul>
    <slot />
  </div>
</template>

<script>
import { ref, provide } from "vue";

export default {
  setup(props, { slots }) {
    const tabTitles = ref(slots.default().map((tab) => tab.props.title));
    const selectedTitle = ref(tabTitles.value[0]);

    provide("selectedTitle", selectedTitle);

    return {
      tabTitles,
      selectedTitle,
    };
  },
};
</script>

<style scoped>
.tabs {
  max-width: 100%;
  margin: 20px;
}

.tabs__heeader {
  margin-bottom: 20px;
  list-style: none;
  display: flex;
  padding: 0;
}

.tabs__heeader li {
  padding: 12px;
  margin-right: 10px;
  background-color: #ddd;
  border-radius: 8px;
  cursor: pointer;
  transition: 0.4s all ease-in-out;
}

.tabs__heeader li.selected {
  background-color: #f77014;
  color: white;
}
</style>