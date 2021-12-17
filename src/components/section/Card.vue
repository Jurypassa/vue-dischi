<template>

    <div class="card">
        <img :src="info.poster" :alt="info.title">
        <p class="white">{{info.title}}</p>
        <p class="gray">{{info.author}}</p>
        <p class="gray">{{info.year}}</p>
    </div>
    
    
        
    
</template>

<script>
export default {
    name: "Card",
    props: {
        info: Object
    }
}
</script>

<style lang="scss" scoped>
@import "../../assets/style/variabili.scss";
    .card{
        display: flex;
        flex-direction: column;
        align-items: center;
    }

        
 
    img{
        width: 80%;
        padding: 20px 0;
    }

    .white{
        color: $white;
        font-weight: bold;
        font-size: 20px;
        padding: 20px 0;
        text-transform: uppercase;
        padding: 0 10px;
        text-align: center;
        padding-bottom: 10px;
        }

    .gray{
        color: $gray;
    }        

   
</style>