<script setup>

 /*const { data } = await useFetch( "http://api.weatherstack.com/current", {
  query: {
    access_key: "a8ce608ceb441b16e2ad14b530bfad80",
    query: "Pretoria"
  }
})
*/

const { data } = await useFetch( "https://api.marketstack.com/v1/eod",
{
 query: {
    access_key: "bb1ce2ee0bcf83a482898b18ef5889e2",
    symbols: "AAPL"
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
    <nav>
    <ul>

      <li><NuxtLink to="/"> About me</NuxtLink>  </li>
      <li><NuxtLink to="/projects"> Past Projects</NuxtLink>  </li>
      <li><NuxtLink to="/contact"> Contacts</NuxtLink>  </li> 
    </ul>
    </nav>
      <NuxtPage />
    </div>
 

  <div class = "block">
			<img src="/Tshego.jpg" height="270" width="190">
	</div>

  <main>
    <h2>About me</h2>
    <p>My name is Tshegofatso Moleme and I am currently a student at the university of pretoria, 
      studying for a Bacherlor's Degree in Information Sciences, specialising in multimedia with 
      the hopes of one day becoming a game developer. Currently, I am familiar in c++, java, web development
      and photoshop and editing</p>
    <p>Currently, my hobbies include reading, listening to music, playing video games and taking walks on the University Campus</p>
  </main>

  <!--
   <h2>Weather in Pretoria</h2>
   <div v-if="data">
      <p>Temperature: {{ data.current.temperature }} °C</p>
      <p>Weather: {{ data.current.weather_descriptions}}</p>
   
    </div> 

  -->

  <h2>Stock data stats</h2>
   <div v-if="data">
      <p>Open: {{ data.data[0].open }}</p>
      <p>Close: {{ data.data[0].close }}</p>
      <p>High: {{ data.data[0].high }}</p>
      <p>Low: {{ data.data[0].low }}</p>
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