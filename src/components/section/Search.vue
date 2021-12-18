<template>
  <div>
      <input type="text" placeholder="Inserisci il nome" v-model="searchText">
      <button class="blue" @click="$emit('search', serchText)">Search</button>
      <button class="orange">Reset</button>
  </div>
</template>

<script>
export default {
    name: "Search",
    data(){
        return{
            serchText: ""
        }
    }
}
</script>

<style lang="scss" scoped>
    input{
        width: 700px;
        height: 30px;
        border-radius: 10px;
    }


    button{
        margin-left: 20px;
        padding: 5px 10px;
        border: none;
        border-radius: 5px;
        font-weight: bold;
        
    }

    .blue{
        background-color: blue;
    }

    .orange{
        background-color: orange;
    }
</style>