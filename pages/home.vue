<template>
  <div id="container">
    <h1 class="title">Galaxy Raiders</h1>
    <div class="menu">
      <div class="list">
        <button class="option">
            <router-link :to="{ name: 'index' }"
              >Iniciar partida</router-link>
        </button>
        <button class="option">
            <router-link to="/scores">Placar</router-link>
        </button>
        <button class="option">
            <router-link to="/exit">Sair</router-link>
        </button>
      </div>
    </div>
  </div>
</template>

<style>
@import url('https://fonts.googleapis.com/css2?family=Press+Start+2P&display=swap');
#container {
  background-image: url("~/assets/space.png");
  height: 100vh;
  width: 100vw;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}
.menu {
  background-color: #36454f;
}
.list {
  position: relative;
  list-style: none;
  padding: 10px;
  margin: 10px;
  list-style-type: none;
  width: 500px;
  display: flex;
  flex-direction: column;
  font-family: 'Roboto', sans-serif;
}
.option {
  position: relative;
  cursor: pointer;
  text-align: center;
  display: list-item;
  margin: 10px;
  z-index: 0;
}
a {
  text-align: center;
  color: #fff;
  text-transform: uppercase;
  text-decoration: none;
}
button:hover {
  background: #494f77;
}
.title {
  color: #fff;
  margin: 20px;
  font-family: 'Press Start 2P', sans-serif;
}
</style>

<script>
export default {
  name: "home",
};
</script>