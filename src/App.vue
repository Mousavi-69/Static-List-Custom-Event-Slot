<template>
<my-button>
  <template v-slot:>
test
  </template>
</my-button>
<br><br>
<div class="contaner" >

<product  :image="i.image" :price="i.price" :title="i.title" 
v-for="i in products" :key="i" @on-delete="deletItem">
</product>
  </div>
</template>

<script>
 import product from './components/product.vue'
 import MyButton from './components/MyButton.vue'


export default {
  name: 'App',
  components: {
    product,MyButton
  },
  data(){return{
    products:[{
id:1,
title:"Fjallraven - Foldsack No. 1 Backpack, Fits 15 Laptops",
price:109.95,
image:"https://fakestoreapi.com/img/81fPKd-2AYL._AC_SL1500_.jpg"
},
{
id:2,
title:"Mens Casual Premium Slim Fit T-Shirts ",
price:22.3,
image:"https://fakestoreapi.com/img/71-3HjGNDUL._AC_SY879._SX._UX._SY._UY_.jpg"
},
{
id:3,
title:"Mens Cotton Jacket",
price:55.99,
image:"https://fakestoreapi.com/img/71li-ujtlUL._AC_UX679_.jpg"
},
{
id:4,
title:"Mens Casual Slim Fit",
price:15.99,
image:"https://fakestoreapi.com/img/71YXzeOuslL._AC_UY879_.jpg"
},
{
id:5,
title:"John Hardy Women's Legends Naga Gold & Silver Dragon Station Chain Bracelet",
price:695,
image:"https://fakestoreapi.com/img/71pWzhdJNwL._AC_UL640_QL65_ML3_.jpg"
},{
id:1,
title:"Fjallraven - Foldsack No. 1 Backpack, Fits 15 Laptops",
price:109.95,
image:"https://fakestoreapi.com/img/81fPKd-2AYL._AC_SL1500_.jpg"
},
{
id:2,
title:"Mens Casual Premium Slim Fit T-Shirts ",
price:22.3,
image:"https://fakestoreapi.com/img/71-3HjGNDUL._AC_SY879._SX._UX._SY._UY_.jpg"
},
{
id:3,
title:"Mens Cotton Jacket",
price:55.99,
image:"https://fakestoreapi.com/img/71li-ujtlUL._AC_UX679_.jpg"
},
{
id:4,
title:"Mens Casual Slim Fit",
price:15.99,
image:"https://fakestoreapi.com/img/71YXzeOuslL._AC_UY879_.jpg"
},
{
id:5,
title:"John Hardy Women's Legends Naga Gold & Silver Dragon Station Chain Bracelet",
price:695,
image:"https://fakestoreapi.com/img/71pWzhdJNwL._AC_UL640_QL65_ML3_.jpg"
}],

  }

  },
  methods:{
deletItem(){
 
}
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
.contaner{
  display: flex;
    flex-direction: row;
    flex-wrap: wrap;
    justify-content: center;
}
</style>
