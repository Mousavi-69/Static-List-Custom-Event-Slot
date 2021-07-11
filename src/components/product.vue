<template>
    <div class="list" >
      <div class="container" v-if="show==true">
          <div class="p-btn">
            <button @click="deletItem" ></button>

          </div>
        <img class="image" :src="image" />
        <h4 class="title">{{ title }}</h4>
        <h5 class="price">{{ price }}$</h5>
      </div>
    </div>
  </template>
  
  <script>
  export default {
      props:["image","title","price"],

   data(){
   return{
show:true,
   }
  },
  methods:{
deletItem(){
this.show=false
    this.$emit("on-delete")
}
  }
  }
  </script>
  
  <style>
  .list {
    display: flex;
    flex-direction: row;
    flex-wrap: wrap;
    justify-content: center;
  }
  .container {
    box-shadow: 0px 0px 5px 5px #ddd;
    border-radius: 16px;
    width: 200px;
    padding: 16px;
    margin: 16px;
  }
  .image {
    width: 184px;
    height: 184px;
    object-fit: contain;
    border-radius: 16px;
  }
  .title {
  }
  .price {
    color: #777;
  }
  button{
      background-color: red;
      border: none;
      width: 15px;
      height: 15px;
      border-radius: 50%;
      
  }
  .p-btn{
      display: flex;
      justify-content: flex-end;
  }
  </style>