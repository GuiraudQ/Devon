<template>
  <div class="leftSide">
    <div class="cards" v-if="!started">
      <PlayerLobby v-for="(player, index) in players" :key="index" :name="player.name" :life="player.maxHp" :attack="player.attack" :src="player.smallImgSrc"></PlayerLobby>
    </div>
  </div>
</template>

<script>
import PlayerLobby from './components/PlayerLobby.vue'

export default {
  components: {
    PlayerLobby
  },
  data(){
    return{
      started:false,
      players:{
        "mano": {
          "id": '1',
          "name": "Mano",
          "nameR": "Mano",
          
          "description": `25 DPS, peux faire des gros crit seulement quand il vien en cours c'est rare`,
          "largeImgSrc": "./assets/images/mano2.png",
          "smallImgSrc": "./assets/images/mano2.png",
          "maxHp": 80,
          "currentHp": 80,
          "attack": 25,
          "crit": 20,
          "degCrit": 500, //500% des degat de base quand il crit
          "sort" : "retard SUPREME",
          "selection" : false,
        },
        "mathieu": {
          "id": '2',
          "name": "Mathieu",
          "nameR": "Mathieu",

          "description": `10 DPS reduit les degat`,
          "largeImgSrc": './assets/images/donconnor.png',
          "smallImgSrc": '../assets/images/donconnor.png',
          "maxHp": 120,
          "currentHp": 120,
          "attack": 10,
          "crit": 25,
          "degCrit": 200,
          "sort" : "Linux attack",
          "selection" : false,
        },  
        "flo": {
          "id": '3',
          "name": "Flo",
          "nameR": "Flo",
          
          "description": `20 DPS Prend les degat pour ses allié`,
          "largeImgSrc": './assets/images/flo2.png',
          "smallImgSrc": '../assets/images/flo2.png',
          "maxHp": 200,
          "currentHp": 200,
          "attack": 20,
          "crit": 5,
          "degCrit": 200,
          "sort" : "mur de cassoulet",
          "selection" : false,
        },
        "dimitri": {
          "id": '4',
          "name": "Dimitri",
          "nameR": "Dimitri",
          
          "description": `15 DPS gros taux crit`,
          "largeImgSrc": './assets/images/Dimitri.jpg',
          "smallImgSrc": "../assets/images/Dimitri.jpg",
          "maxHp": 100,
          "currentHp": 100,
          "attack": 15,
          "crit": 80,
          "degCrit": 250,
          "sort" : "parle de scooteur electrique",
          "selection" : false,
        },
        "quentin": {
          "id": '5',
          "name": "Quentin",
          "nameR": "Quentin",
          
          "description": `15 DPS, augmente les degat des allié`,
          "largeImgSrc": './assets/images/Quentin.jpg',
          "smallImgSrc": '../assets/images/quentin.png',
          "maxHp": 90,
          "currentHp": 90,
          "attack": 15,
          "crit": 30,
          "degCrit": 200,
          "sort" : "vole les cookies",
          "selection" : false,
        },
        "laza": {
          "id": '6',
          "name": "Laza",
          "nameR": "Laza",
          
          "description": `15 HPS soigne ses alliés du nombre de ses degats`,
          "largeImgSrc": './assets/images/Laza.jpg',
          "smallImgSrc": '../assets/images/Laza.jpg',
          "maxHp": 120,
          "currentHp": 120,
          "attack": 15,
          "crit": 50,
          "degCrit": 400,
          "sort" : "Roulage de bus",
          "selection" : false,
        },
        "lucas": {
          "id": '7',
          "name": "Lucas",
          "nameR": "Lucas",
          
          "description": `15 DPS, peux bloquer une attaque`,
          "largeImgSrc": './assets/images/Lucas.jpg',
          "smallImgSrc": '../assets/images/lucas.png',
          "maxHp": 110,
          "currentHp": 110,
          "attack": 15,
          "crit": 30,
          "degCrit": 200,
          "sort" : "Head SHOT",
          "selection" : false,
        },
        "youssef": {
          "id": '8',
          "name": "Youssef",
          "nameR": "Youssef",
          
          "description": `prend les degat de ses allié`,
          "largeImgSrc": './assets/images/Youssef.jpg',
          "smallImgSrc": '../assets/images/Youssef.jpg',
          "maxHp": 125,
          "currentHp": 125,
          "attack": 0,
          "crit": 50,
          "degCrit": 300,
          "sort" : "Invinsible",
          "selection" : false,
        },
      }
    }
  },
}
</script>

<style scoped>
  .leftSide{
    width: 30vw;
    min-height: 100vh;
  }
  .cards{
    display: flex;
    justify-content: space-around;
    align-items: flex-start;
    flex-wrap: wrap;
  }

</style>>