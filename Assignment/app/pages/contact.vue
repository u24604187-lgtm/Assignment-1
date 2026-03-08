<script>

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
    <h2>Contact Information</h2>
    <p>If you want to speak further, fill in your information so I may contact you as soon as I receive your details</p>

    <form name="contact" methods="POST" data-netlify="true" onSunmit="submit">
		<div class="form">
			<fieldset>
			<legend>Personal Details</legend>
			<label for="name">Name:</label>
			<input type="text" id="name" name="namePerson" > <br/><br/>
			<label for="name">Surname:</label>
			<input type="text" id="surname" name="surnamePerson" ><br/><br/>
			<label for="dob">Date of Birth:</label>
			<input type="date" id="dob" name="dob"> <br/> <br/>

				<legend>Contact Details</legend>
				<p>Choose your preferred contact method</p>
				<input type="radio" id="whatsapp" name="preferred" value="WhatsApp">
				<label for="whatsapp">WhatsApp</label> 
				<input type="radio" id="email" name="preferred" value="email">
				<label for="email">E-mail</label> 
				<input type="radio" id="sms" name="preferred" value="SMS" >
				<label for="sms">SMS</label> <br/>

				<label for="email">Enter your e-mail:</label>
				<input type="email" min="8" max="20" id="email" name="email"> <br/><br/>
				<label for="number">Cellphone number:</label>
				<input type="text" min="0" max="10" id="number" name="number">
			</fieldset> <br/>

			<input type="button" value="Submit" class="button">
		</div>
			
		</form>
  </main>

    
    <!--
   <NuxtRouteAnnouncer />
    <NuxtWelcome /> -->
  </div>
</template>

<style scoped>

  .button{
    border-radius: 10%;
    padding: 10px;
    background-color: rgb(212, 164, 209);
    font-size: 15px;
    color: #f9ddf8;
    border-color: #f9ddf8;
  }

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