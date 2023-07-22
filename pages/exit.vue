<template>
    <div id = "container">
        <div class="spaceship"></div>
        <h1 class="titleclose">Galaxy Raiders</h1>
    </div>

</template>

<style>
@import url('https://fonts.googleapis.com/css2?family=Press+Start+2P&display=swap');
#container {
    background-image: url("~/assets/space.png");
    height: 100vh;
    width: 100vw;
    display: flex;
    justify-content: center;
    align-items: center;
}
.titleclose {
    margin: 20px;
    font-family: 'Press Start 2P', sans-serif;
}
.spaceship {
    background-image: url("~/assets/spaceship.png");
    width: 90px;
    height: 48px;
    background-repeat: no-repeat;
}
</style>

<script>          
export default {
  name: "exit",
};
</script>