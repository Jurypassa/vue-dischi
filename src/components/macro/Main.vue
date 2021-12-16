<template>
  <main>
      <div class="container">
          <div class="row">
              <div class="col-12 col-sm-6 col-lg-2 offset-lg-1">
                  <Card/>
              </div>
              <div class="col-12 col-sm-6 col-lg-2 offset-lg-1">
                  <Card/>
              </div>
              <div class="col-12 col-sm-6 col-lg-2 offset-lg-1">
                  <Card/>
              </div>
              <div class="col-12 col-sm-6 col-lg-2 offset-lg-1">
                  <Card/>
              </div>
              <div class="col-12 col-sm-6 col-lg-2 offset-lg-1">
                  <Card/>
              </div>
              
          </div>
      </div>
  </main>
</template>

<script>
import Card from "../section/Card.vue";
export default {
    name: "Main",
    components: {
        Card
    }
}
</script>

<style lang="scss" scoped>
    main{
        height: calc(100vh - 100px);
        background-color: #1e2d3b;
    }

    .container{
        background-color: yellow;
    }

</style>