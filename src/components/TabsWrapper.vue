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
  max-width: 400px;
  margin: 0 auto;
}

.tabs__heeader {
  margin-bottom: 10px;
  list-style: none;
  padding: 0;
  display: flex;
}

.tabs__heeader li {
  width: 80px;
  text-align: center;
  padding: 10px 20px;
  margin-right: 10px;
  background-color: #ddd;
  border-radius: 8px;
  cursor: pointer;
  transition: 0.4s all ease-in-out;
}

.tabs__heeader li.selected {
  background-color: green;
  color: white;
}
</style>