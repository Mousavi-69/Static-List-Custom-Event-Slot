<template>
  <button >
      <slot></slot>
  </button>
</template>

<script>
export default {

}
</script>

<style scoped>
button{

    width: 100px;
    height: 40px;
    padding: 8px;
    background-color: rgb(37, 131, 175);
    color: black;
    border-radius: 8px;
}
</style>