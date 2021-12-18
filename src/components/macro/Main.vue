<template>
  <main>
      <div class="container">
            <div class="serchBar">
                <Search @search="searchAlbums"/>
            </div>
            
            <div class="flex">
                <div class="box" v-for="(card, index) in cards" :key="index">
                <Card :info="card"/>
                </div>
            </div>
            
        </div>
  </main>
</template>

<script>
import axios from "axios";
import Card from "../section/Card.vue";
import Search from "../section/Search.vue";

export default {
    name: "Main",
    components: {
        Card,
        Search
    },
    data(){
        return{
            cards: null,
            searchText: ""
        }
    },
    created(){
        axios.get('https://flynn.boolean.careers/exercises/api/array/music')
        .then((response) => {
            // handle success
            this.cards = response.data.response;
        })
        .catch(function (error) {
            // handle error
            console.log(error);
        })
    },
    methods: {
        searchAlbums(payload){
            this.searchText = payload;
        }
    },
    computed: {
        cardFiltered(){
            const arrayFiltered = this.cards.filter( (elm) => {
                return  elm.title.toLowerCase().includes(this.searchText.toLowerCase());
            });
            return arrayFiltered;
        }
    }
}
</script>

<style lang="scss" scoped>
    main{
        height: calc(100vh - 100px);
        background-color: #1e2d3b;
    }

    .container{
        width: 60%;
        margin: 0 auto;
        padding-top: 100px;

        .serchBar{
            padding-bottom: 50px;
        }

        .flex{
            display: flex;
            justify-content: space-between;
            flex-wrap: wrap;
        }

        .box{
            background-color: #2e3a46;
            width: calc(100% / 5 - 25px);
            margin-bottom: 20px;
            min-height: 350px;
        }
    }

</style>