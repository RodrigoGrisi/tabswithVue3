<template>
  <div class="sidebar">
    <div class="menu-item" v-for="item in menuItems" :key="item.name">
      <i :class="item.icon"></i>
      <span>{{ item.name }}</span>
    </div>
  </div>
</template>

<script>
export default {
  name: "Sidebar",
  data() {
    return {
      menuItems: [
        { name: "Home", icon: "fa fa-home" },
        { name: "Entregas", icon: "fa fa-truck" },
        { name: "Notas Fiscais", icon: "fa fa-file-invoice" },
      ],
    };
  },
};
</script>

<style scoped>
.sidebar {
  width: 220px;
  background-color: #433d3d; /* Cinza claro */
  display: flex;
  height: 100vh;
  flex-direction: column;
  align-items: center;
  padding-top: 20px;
}

.menu-item {
  width: 100%;
  padding: 15px;
  display: flex;
  align-items: center;
  justify-content: flex-start;
  color: #f77014;
  cursor: pointer;
  transition: background-color 0.3s;
  gap: 20px;
}

.menu-item:hover {
  background-color: #e33c08;
  color: white; /* Azul claro */
}
.menu-item i {
  font-size: 30px;
}
</style>
