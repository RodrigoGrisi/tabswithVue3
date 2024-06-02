<template>
  <Layout>
    <Sidebar />
    <div class="content">
      <AlertsAndNews />
      <TabsWrapper>
        <Tab title="Cadastrar Motorista"><Form /></Tab>
        <Tab title="Inventário">Content of Tab 2</Tab>
        <Tab title="Pedidos">Content of Tab 3</Tab>
        <Tab title="Gestão de Armazém">Content of Tab 4</Tab>
        <Tab title="Gestão de Fornecedores">Content of Tab 5</Tab>
        <Tab title="Gestão de Clientes">Content of Tab 6</Tab>
        <Tab title="Gestão Financeira">Content of Tab 7</Tab>
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
import AlertsAndNews from "./components/AlertsAndNews.vue";
import "@fortawesome/fontawesome-free/css/all.css";
import "@fortawesome/fontawesome-free/js/all.js";
</script>

<style scoped>
.content {
  width: 100%;
  height: 100vh;
}
</style>