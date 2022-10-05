<template>
  <header>
    <h1>More on Vue Components</h1>
  </header>
</template>
<script>
export default {
    name: 'TheHeader'
};
</script>
<style lang="scss" scoped>
  header {
    width: 100%;
    height: 5rem;
    display: flex;
    justify-content: center;
    align-items: center;
    background-color: #000000;
  }

  header h1 {
    color: white;
    margin: 0;
  }
</style>