<template>
  <div class="container">
    <header><h1>Ambience</h1></header>
        <!-- <div @click="play()">
          Hello
          <audio id="audio" :src="birds">
          </audio>
        </div> -->
    <div class="icon-container">
      <div class="icon-column">
          <img src="../assets/Thunder.svg" @click="(e) => play(e)" ambience="thunder" status="off">
          <audio id="thunder" :src="thunder" ></audio>

          <img src="../assets/Birds.svg" @click="(e) => play(e)" ambience="birds" status="off">
          <audio id="birds" :src="birds"></audio>

          <img src="../assets/Ocean.svg" @click="(e) => play(e)" ambience="ocean" status="off">
          <audio id="ocean" :src="ocean"></audio>

          <img src="../assets/Wind.svg" @click="(e) => play(e)" ambience="wind" status="off">
          <audio id="wind" :src="wind"></audio>
      </div>

      <div class="icon-column">
        <img src="../assets/Rain.svg" @click="(e) => play(e)" ambience="rain" status="off">
        <audio id="rain" :src="rain"></audio>

        <img src="../assets/Cafe.svg" @click="(e) => play(e)" ambience="cafe" status="off">
        <audio id="cafe" :src="cafe"></audio>

        <img src="../assets/Crickets.svg" @click="(e) => play(e)" ambience="crickets" status="off">
        <audio id="crickets" :src="crickets"></audio>

        <img src="../assets/Fire.svg" @click="(e) => play(e)" ambience="fire" status="off">
        <audio id="fire" :src="fire"></audio>

      </div>
    </div>
  </div>
</template>

<script>

export default {
  name: 'Ambience',
  data() {
    return {
      thunder: require('../assets/sounds/Thunder.mp3'),
      birds: require('../assets/sounds/Birds.mp3'),
      cafe: require('../assets/sounds/Cafe.mp3'),
      crickets: require('../assets/sounds/Crickets.mp3'),
      fire: require('../assets/sounds/Fire.mp3'),
      ocean: require('../assets/sounds/Ocean.mp3'),
      rain: require('../assets/sounds/Rain.mp3'),
      wind: require('../assets/sounds/Wind.mp3'),
    }
  },
  methods: {
    play(e) {
      console.log('hit');
      
      if(e.target.attributes.status.value === 'off') {
        e.target.attributes.status.value = 'on';
        document.getElementById(e.target.attributes.ambience.value).play()
      } else if (e.target.attributes.status.value === 'on') {
        e.target.attributes.status.value = 'off';
        document.getElementById(e.target.attributes.ambience.value).pause()
      }

    }
  }
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
  cursor:pointer;
}

</style>
