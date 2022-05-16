<template>
  <div>
    <div class="container">

      <ul>
         <li v-for="(item, index) in dataBlu" :key="`dataBlu-${index}`">
           <div class="box-img">
             <img :src="item.img" alt="xxx">
           </div>
            <a href="#">{{item.nome}}</a>
         </li>
       </ul>

    </div>

  </div>
</template>

<script>
export default {
  name: "BlueSection",
  data(){
    return{
      dataBlu:[
        {nome: "Digital comics",
         img: require("../assets/img/buy-comics-digital-comics.png")
        },
        {nome: "Dc merchandise",
         img: require("../assets/img/buy-comics-merchandise.png")
        },
        {nome: "subscription",
         img: require("../assets/img/buy-comics-subscriptions.png")
        },
        {nome: "comic shop locator",
         img: require("../assets/img/buy-comics-shop-locator.png")
        },
        {nome: "dc power visa",
         img: require("../assets/img/buy-dc-power-visa.svg")
        },
       
       
        
       
      ]
    }
  }
}
</script>

<style lang="scss" scoped>
@import "../assets/style/vars";
@import "../assets/style/general.scss";
div{
  min-height:150px;
  background-color: $primary-color;
  color: white;
  display: flex;
  align-items: center;
  font-size: 12px;
  
  .box-img{
    width: 40px;
    margin: 0 20px;
  }
  ul{
      display: flex;
      li{
        display: flex;
        align-items: center;
        list-style: none;
        margin-right: 30px;
        a{
          text-transform: uppercase;
          text-decoration: none;
          color: white
        }
      }
  }
}

</style>