<template>
  <Layout>
    <Sidebar />
    <div class="content">
      <TabsWrapper>
        <Tab title="Tab 1"><Form /></Tab>
        <Tab title="Tab 2">Content of Tab 2</Tab>
        <Tab title="Tab 3">Content of Tab 3</Tab>
      </TabsWrapper>
    </div>
  </Layout>
</template>

<script setup>
import Tab from "./components/Tab.vue";
import TabsWrapper from "./components/TabsWrapper.vue";
import Layout from "./components/Layout.vue";
import Sidebar from "./components/Sidebar.vue";
import Form from "./components/Form.vue";
import "@fortawesome/fontawesome-free/css/all.css";
import "@fortawesome/fontawesome-free/js/all.js";
</script>

<style scoped>
.content {
  width: 100%;
  height: 100vh;
}
</style>