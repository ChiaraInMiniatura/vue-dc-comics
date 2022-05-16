<template>
  <header>
    <div class="container">

      <div class="box-logo">
        <img src="../assets/img/dc-logo.png" alt="logo">
      </div>
      <div class="h-menu ">
        <ul>
          <li v-for="(item, index) in menu" :key="`menu-${index}`">
             <a :class="{'active':item.isActive}" href="#">{{item.nome}}</a>
          </li>
        </ul>
        
      </div>

    </div>
  </header>
</template>

<script>
export default {
  name: "HeaderComponent",
  data(){
    return{
      menu:[
        {nome: "Characters",
        isActive: false,
        },
        {nome: "Comics",
        isActive: true,
        },
        {nome: "Movies",
        isActive: false,
        },
        {nome: "Tv",
        isActive: false,
        },
        {nome: "Games",
        isActive: false,
        },
        {nome: "Collectibles",
        isActive: false,
        },
        {nome: "Videos",
        isActive: false,
        },
        {nome: "Fans",
        isActive: false,
        },
        {nome: "News",
        isActive: false,
        },
        {nome: "Shop",
        isActive: false,
        },
      ]
    }
  }
}
</script>

<style lang="scss" scoped>
@import "../assets/style/vars";

header{
  .container{

    min-height: 100px ;
    display: flex;
    justify-content: space-between;
    align-items: center;
    font-size: 12px;
    .box-logo{
      margin: 20px;
      width: 70px;
    }
    .h-menu{
      ul{
        display: flex;
        li{
          list-style: none;
          margin-right: 20px;
          a{
            text-transform: uppercase;
            text-decoration: none;
            padding: 35px 0;
            color: black;
            &:hover{
            color: $primary-color ;
            }
            &.active{
            color: $primary-color;
            border-bottom: 3px solid $primary-color;
            }
          }
  }
      }
    
    }

  
  }
}
</style>