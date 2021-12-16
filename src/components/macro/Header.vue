<template>
  <header>
      <img src="https://play-lh.googleusercontent.com/UrY7BAZ-XfXGpfkeWg0zCCeo-7ras4DCoRalC_WXXWTK9q5b0Iw7B0YQMsVxZaNB7DM" alt="logo spotify">
  </header>
</template>

<script>
export default {
  name: "Header"
}
</script>

<style lang="scss" scoped>
  header{
    height: 100px;
    background-color: #2e3a46;
    display: flex;
    align-items: center;

    img{
      width: 60px;
      margin-left:20px ;
    }
  }
</style>