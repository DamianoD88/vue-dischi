<template>
  <header>
      <!-- <h1>{{ message }}</h1> -->
      <img class="logo rounded-circle" src="../../img/logo.png" alt="">
  </header>
</template>

<script>
export default {
    name: 'Header',
    // props: ["message"]
}
</script>

<style lang="scss" scoped>

header {
    width: 100%;
    height: 70px;
    background-color: #2e3a46;

    .logo {
        width: 40px;
        margin: 15px;
    }
}

</style>