<script setup>

const { data } = await useFetch( "http://api.weatherstack.com/current", {
  query: {
    access_key: "a8ce608ceb441b16e2ad14b530bfad80",
    query: "Pretoria"
  }
})

</script>

<template>
  <div class="html">

  <header>
    <h1>Tshegofatso's Portfolio page</h1>
    <p></p>
  </header>

  <div class="nav">
    <ul>

      <li><NuxtLink to="/"> About me</NuxtLink>  </li>
      <li><NuxtLink to="/projects"> Past Projects</NuxtLink>  </li>
      <li><NuxtLink to="/contact"> Contacts</NuxtLink>  </li> 

    </ul>
  </div>

  <main>
    <h3>Tic Tac Game</h3>
    <p>I have created a simple Tic Tac Toe game with the use of c++. This was a rudimentary game
        using the most basic attributes of c++ and was used to further my understanding of if-statements
    </p>

    <h3>Animation</h3>
    <p>I have created an animation with adobe animate based on my favourite soundtrack from the popular
        animated show called Steven Universe </p>

    <h3>Comic book</h3>
    <p>I have created a short comic book about a character named Desmond who has powers
        against his wills. The comic book name is the character's namesake and it is not
        released yet.
    </p>
  </main>

  <h2>Weather in Pretoria</h2>
   <div v-if="data">
      <p>Temperature: {{ data.current.temperature }} °C</p>
      <p>Weather: {{ data.current.weather_descriptions}}</p>
   
    </div> 


    
    <!--
   <NuxtRouteAnnouncer />
    <NuxtWelcome /> -->
  </div>
</template>

<style scoped>

  .nav ul{
      margin:5px;
      padding:10px;
      display:flex;
      justify-content:center;
      list-style-type: none;
          }

    li{
      margin:2px;
      padding:5px;
      }

    a{
      text-decoration:none;
      color:rgb(121, 102, 245);
				}

    .html{
      background-color: rgb(243, 227, 203);
      }

            
      body{
      /* background-color:#F5E0F5;*/
      font-size:16px;
      font-family:DM Sans,monospace,sans-serif;
      padding:20px;
      margin-left: 200px;
      margin-right: 200px;
      }

      .nav a:hover{
        font-style: italic;
        text-decoration: underline;
        color: #e6b1e4;
        background-color: rgba(91, 9, 84, 0.5);
        border-radius: 10px;
        margin: 20px auto;
        width: fit-content;
        padding: 10px 20px;
      }

      header {
        text-align: center;
        background-color: rgba(91, 9, 84, 0.5);
        padding: 20px;
        border-radius: 10px;
        color: #dcdcdc;
      }

      header h1 {
        font-size: 44px;
        margin-bottom: 10px;
      }

       h2{
         font-size: 26px;
        margin-bottom: 10px;
        text-decoration: underline;
         color: rgb(121, 102, 245);
      }

      header p {
        font-size: 20px;
        font-style: italic;

      }

      p{
        color: rgb(234, 118, 226);
      }

</style>