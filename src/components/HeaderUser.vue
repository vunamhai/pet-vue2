<template>
  <div class="hello tit">
    <nav class="navbar navbar-expand-lg navbar-light bg-light"  >
  <div class="container-fluid">
     <a class="navbar-brand" href="#/login">
      <img   src="https://img.freepik.com/free-vector/pet-shop-paw-logo_142351-10.jpg" width="150" height="70"/>
    </a>
    <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
      <span class="navbar-toggler-icon"></span>
    </button>
    <div class="  bar collapse navbar-collapse" id="navbarSupportedContent">
      <ul class="navbar-nav me-auto mb-2 mb-lg-0">
        <li class="nav-item">
          <a class="     active" ali aria-current="page" href="#/login">Home</a>
        </li>
        <li class="nav-item dropdown">
          <a class=" dropdown-toggle " href="#" id="navbarDropdown" role="button" data-bs-toggle="dropdown" aria-expanded="false">
            About
          </a>
          <ul class="dropdown-menu " aria-labelledby="navbarDropdown">
            <li><a class="dropdown-item" href="#">About Us</a></li>
            <li><a class="dropdown-item" href="#">The Diffirence</a></li>
            <li><a class="dropdown-item" href="#">Our Team </a></li>
            <li><a class="dropdown-item" href="#">VIPET Program </a></li>
          </ul>
        </li>
        
        <li class="nav-item dropdown">
          <a class=" dropdown-toggle" href="#" id="navbarDropdown" role="button" data-bs-toggle="dropdown" aria-expanded="false">
            Veterinary
          </a>
          <ul class="dropdown-menu" aria-labelledby="navbarDropdown">
            <li><a class="dropdown-item" href="#">Surgery</a></li>
            <li><a class="dropdown-item" href="#">Diagnostics</a></li>
            <li><a class="dropdown-item" href="#">Dental Care</a></li>
            <li><a class="dropdown-item" href="#">Health Check</a></li>
            <li><a class="dropdown-item" href="#">Parasite Control</a></li>
            <li><a class="dropdown-item" href="#">Pet Travel </a></li>
            <li><a class="dropdown-item" href="#">Grooming </a></li>
            <li><a class="dropdown-item" href="#">Boarding </a></li>
          </ul>
        </li>
        
        <li class="nav-item dropdown">
          <a class=" dropdown-toggle" href="#" id="navbarDropdown" role="button" data-bs-toggle="dropdown" aria-expanded="false">
            Dog Traning
          </a>
          <ul class="dropdown-menu" aria-labelledby="navbarDropdown">
            <li><a class="dropdown-item" href="#">Mark Singer </a></li>
            <li><a class="dropdown-item" href="#">Private Lessons</a></li>
            <li><a class="dropdown-item" href="#">In-home Behavioral Consultations </a></li>
            <li><a class="dropdown-item" href="#">Puppy Classes</a></li>
            <li><a class="dropdown-item" href="#">Group Obedience Services</a></li>
            <li><a class="dropdown-item" href="#">Specialist Services</a></li>
            <li><a class="dropdown-item" href="#">Seminar & Workshop </a></li>
          </ul>
        </li>
        <li class="nav-item dropdown">
          <a class=" dropdown-toggle" href="#" id="navbarDropdown" role="button" data-bs-toggle="dropdown" aria-expanded="false">
            Blog
          </a>
          <ul class="dropdown-menu" aria-labelledby="navbarDropdown">
            <li><a class="dropdown-item" href="#">Blog</a></li>
            <li><a class="dropdown-item" href="#">Events</a></li>
          </ul>
        </li>
        <li class="nav-item">
          <a class=" active" ali aria-current="page" href="#">Contact</a>
        </li>
      </ul>
      <form class="d-flex">
        <button type="button"  class="btn btn-outline-danger">Book Appointment</button>
      
      </form>
    </div>
  </div>
</nav>
  </div>
</template>



<script>
export default {
  name: 'HeaderUser',
  props: {
    msg: String
  }
}

</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped >
.bar{
  padding-left: 10%;
}
a{
  color: black; 
 
}
a:hover{
background-color: whitesmoke;
  color: red;
}
.btn {
  border-radius: 40px;
  text-transform: uppercase;  
  width: 200px;
  margin-left: 30px;
}
.tit{
    font-family: "BarlowCondensed",sans-serif;
    font-weight: 750;
    line-height: 1.3;
    font-size: 18px;
    margin-bottom: 450px;
    color:aliceblue;
    padding-left : 600px
    
}

.nav-item {
margin-left: 10px;
}
.btn {
  margin-right: 80px;
  width: 200px;
  height: 50px;
}
.navbar{
  border:1px solid #000000;
   background-image: url(https://www.theanimaldoctors.org/wp-content/themes/tad/assets/images/cream-texture.jpg);
  padding-top: 2px ;
}

@import url(https://fonts.googleapis.com/css?family=Lato);

*, *:before, *:after{
  -webkit-box-sizing: border-box;
  -moz-box-sizing: border-box;
  box-sizing: border-box;
  padding: 0;
  margin: 0;
  font-family: 'Lato', sans-serif;
}

/*| Navigation |*/

nav{
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  background: #fff;
  box-shadow: 0 3px 10px -2px rgba(0,0,0,.1);
  border: 1px solid rgba(0,0,0,.1);
}
  nav ul{
    list-style: none;
    position: relative;
    float: right;
    margin-right: 100px;
    display: inline-table;
  }
    nav ul li{
      float: left;
      -webkit-transition: all .2s ease-in-out;
      -moz-transition: all .2s ease-in-out;
      transition: all .2s ease-in-out;
    }

    nav ul li:hover{background: rgba(0,0,0,.15);}
    nav ul li:hover > ul{display: block;}
    nav ul li{
      float: left;
      -webkit-transition: all .2s ease-in-out;
      -moz-transition: all .2s ease-in-out;
      transition: all .2s ease-in-out;
    }
      nav ul li a{
        display: block; 
        padding: 30px 20px;
        color: #222; 
        font-size: .9em;
        letter-spacing: 1px;
        text-decoration: none;
        text-transform: uppercase;
      }
      nav ul ul{
        display: none;
        background: #fff;
        position: absolute; 
        top: 100%;
        box-shadow: -3px 3px 10px -2px rgba(0,0,0,.1);
        border: 1px solid rgba(0,0,0,.1);
      }
        nav ul ul li{float: none; position: relative;}
          nav ul ul li a {
            padding: 15px 30px; 
            border-bottom: 1px solid rgba(0,0,0,.05);
          }
          nav ul ul ul {
            position: absolute; 
            left: 100%; 
            top:0;
          }
</style>
