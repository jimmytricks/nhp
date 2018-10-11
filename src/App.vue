<template>
  <div id="app">
    <img src="./assets/logo.png">
    <router-view/>
  </div>
</template>

<script>
export default {
  name: 'App'
}
</script>

<script>
let loadedJSON;

// new player constuctor that takes name, ID, total goals? Have myJSON run new player constructor for each person 

let playerList;
fetch('https://statsapi.web.nhl.com/api/v1/teams?expand=team.roster')
  .then(function(response) {
    return response.json();
  })
     .then(function(myJson){
    for (let i = 0; i < myJson.teams.length; i++){
      myJson
      console.log(i);
    }
    });

  // function getPlayerIDAndName(myJson) {
  //   for (let i = 0; i > myJson.teams.length;  i++){
  //     console.log(i);
  //   }
  // }

    //  .then(function(myJson){
    //  debugger;
    // for (let i = 0; i > myJson.teams.length; i++){
    //   console.log(i);
    // }
    // });

  // myJson.teams[""0""].roster.roster

  // // for each teams, roster, roster(loop through this array) - index - person, full name & ID
  // myJson.teams[""0""].roster.roster[""0""].person.fullName



</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
