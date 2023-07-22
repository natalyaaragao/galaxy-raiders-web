<template>
  <div id="container">
    <h1 class="title">Galaxy Raiders</h1>
    <div class="users">
      <table>
        <caption>Leaderboard</caption>
        <tr>
          <th></th>
          <th>date/time</th>
          <th>asteroids</th>
          <th>total</th>
        </tr>
        <tr v-for="user in users" :key="user.id">
         <td class = "item-numbers"> {{user.id}} </td>
         <td class = "item-date"> {{user.date_time}} </td>
         <td class = "item-numbers"> {{user.asteroids}} </td>
         <td class = "item-numbers"> {{user.total}} </td>
        </tr>
      </table>
      <button class="button-back">
      <router-link :to="{ name: 'home' }"
              >Voltar</router-link>
      </button>
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
  color: #fff;
  font-family: 'Roboto', sans-serif;
}
.item-numbers {
  font-weight: 600;
  background: #536872;
}
.item-date {
  background: #536872;
  padding: 0 40px 0 50px;
}
.users {
  background-color: #36454f;
  padding: 10px;
}
table {
  color: #fff;
  width: 500px;
  font-size: 1.2em;
  margin: 10px;
}
th {
  font-weight: 200;
  color: #e5e5e5;
  text-transform: uppercase;
  letter-spacing: .2rem;
}
tr {
  margin: 15px;
}
th, td {
  padding: 8px;
  text-align: center;
  border-bottom: 1px solid #ddd;
}
td:hover {
  background-color: #777b99;
}
caption {
  font-weight: 800;
  text-transform: uppercase;
  font-size: 1.5em;
  color: #708090;
  background: #fff;
  letter-spacing: .2rem;
}
.button-back {
  margin: 10px;
}
.title {
  color: #fff;
  margin: 20px;
  font-family: 'Press Start 2P', sans-serif;
}
</style>


<script>

import userData from './Leaderboard.json'

export default {
  name: "scores",
  data() {
    return {
      users: userData,
    };
  },
};
</script>