<template>
    <div class="card">
        <div class="headerCard">
            <img :src="src" alt="image du joueur">
        </div>
        <div class="bodyCard">
            <h4>{{name}}</h4>
        </div>
        <div class="footerCard">
            <div class="life">{{life}}</div>
            <div class="attack">{{attack}}</div>
        </div>
        <div class="plus">+</div>
    </div>
</template>

<script>
export default {
    props:{
        name:{
            type:String,
            required:true,
        },
        life:{
            type:Number,
            required:true,
        },
        attack:{
            type:Number,
            required:true,
        },
        src:{            
            type:String,
            required:true,}
    },
    methods: {
    },
}
</script>

<style scoped>
    .card{
        width: 100px;
        height: 150px;
        margin: 15px 0;
        display: flex;
        justify-content: center;
        align-items: center;
        flex-direction: column;
    }
    .headerCard{
        width: 100%;
        display: flex;
        justify-content: center;
        align-items: center;
        background: radial-gradient(50% 50% at 50% 50%, #CC5E1F 0%, rgba(30, 30, 30, 0) 100%);
    }
    .headerCard img{
        width: 100%;
        height: 100px;
        object-fit: cover;
    }
    .bodyCard{
        width: 100%;
        text-transform: uppercase;
        text-align: center;
    }
    .footerCard{
        width: 100%;
        display: flex;
        justify-content: space-between;
        align-items: center;
    }
    .plus{
        width: 20px;
        height: 20px;
        display: flex;
        justify-content: center;
        align-items: center;
        padding-bottom: 3px;

        border: 1px solid white;
        border-radius: 100%;
    }
</style>