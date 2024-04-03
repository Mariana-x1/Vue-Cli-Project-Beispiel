<template>
  <header class="header">
    <div class="logo-container">
      <img src="@/assets/logo.jpg" alt="Logo" />
      <h1 class="project-name">Hello Project-BookStore</h1>
    </div>
  </header>
</template>

<script>
export default {
  name: "LayoutHeader",
};
</script>

<style scoped>
.header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 1rem;
  background-color: #333666;
  color: #fff;
}

.logo-container {
  display: grid;
  grid-template-columns: auto auto;
  align-items: center;
  margin-left: 4rem;
}
.logo-container img {
  height: 3rem;
}
.project-name {
  color: #998111;
  margin-left: 4rem;
  font-size: 1.5rem;
}
</style>
