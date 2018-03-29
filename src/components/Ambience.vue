<template>
  <div class="container">
    <header><h1>Ambience</h1></header>
    <div class="icon-container">
      <div class="icon-column">
    <img src="../assets/Thunder.svg">
    <img src="../assets/Rain.svg">
    <img src="../assets/Ocean.svg">
    <img src="../assets/Wind.svg">
    </div>
    <div class="icon-column">
    <img src="../assets/Birds.svg">
    <img src="../assets/Cafe.svg">
    <img src="../assets/Crickets.svg">
    <img src="../assets/Fire.svg">
    <input type="range"/>
    <audio autoplay src="../assets/sounds/Birds.m4a"/> 
    </div>
    </div>
  </div>
</template>

<script>

export default {
  name: 'Ambience',

}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.container, .icon-column {
  display: flex;
  flex-direction: column;
  align-items: center;
}
.icon-container {
  display: flex;
  flex-direction: row;
}
.icon-column:last-of-type {
  margin-left: 55px;
}
img {
  height: 100px;
  width: 100px;
  padding: 20px;
}

</style>
