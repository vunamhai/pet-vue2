<template >

<div class="back">
    <table class="inner-context">
        <tr>
            <td class="left-td" >
                <p  class="lower">  PREMIUM VETERINARY SERVICES FOR ALL PETS AND THEIR OWNERS</p>
        <p class="upper" > WHERE </p>
       <p class="upper" >CARING HAS</p>
       <p class="upper" >NO BOUNDARIES</p>
        <p class = "em"> Animal Doctors International is a full-service veterinary clinic driven by a passion for excellence. We provide compassionate clinical care, state-of-the-art technology and highly-skilled international veterinarians to deliver on our promise of exceptional service and personalised care for your loved pets.</p>
        <p class = "em">Our entire staff are committed to maintaining international standards and treating all animals with loving care in every check-up, procedure or surgery. </p>
       </td>
        <td style=" margin-right: 20px;" >
            <div  id="carouselExampleControls" class="carousel slide" style="height:550.6px" data-bs-ride="carousel">
  <div class="carousel-inner" style="width: 600px">
    <div class="carousel-item active ">
      <img src="https://www.theanimaldoctors.org/wp-content/uploads/2021/05/DSC09945.jpg.webp" class="d-block w-100 " style="height:550.6px"  alt="...">
    </div>
    <div class="carousel-item">
      <img src="https://www.theanimaldoctors.org/wp-content/uploads/2021/05/DSC09932.jpg.webp" class="d-block w-100" style="height:550.6px" alt="...">
    </div>
    <div class="carousel-item">
      <img src="https://www.theanimaldoctors.org/wp-content/uploads/2021/05/DSC09832.jpg.webp" class="d-block w-100"  style="height:550.6px;display: block;  " alt="...">
    </div>
  </div>
  <button class="carousel-control-prev" type="button" data-bs-target="#carouselExampleControls" data-bs-slide="prev">
    <span class="carousel-control-prev-icon" aria-hidden="true"></span>
    <span class="visually-hidden">Previous</span>
  </button>
  <button class="carousel-control-next" type="button" data-bs-target="#carouselExampleControls" data-bs-slide="next">
    <span class="carousel-control-next-icon" aria-hidden="true"></span>
    <span class="visually-hidden">Next</span>
  </button>
</div>
        </td>  
       </tr>     
</table>
        </div >
</template>
<script>

export default {
  name: 'HomePage',
  props: {
    msg: String
  }
}

</script>
<style scoped >

tr{
  max-width: 1000px;
}
.back{
  margin-top: 85px;
   background-image: url(F:\pet\pet-vue\src\assets\homepage.png);
}
.left-td{
  max-width: 600px;
}
.inner-context{
    margin-left: 150px;
    margin-top: 0px;
  .slick-slider .slick-track, .slick-slider .slick-list {
    -moz-transform: translate3d(0,0,0);
    -ms-transform: translate3d(0,0,0);
    -o-transform: translate3d(0,0,0);
     -webkit-transform: translate3d(0,0,0); 
     transform: translate3d(0,0,0); 
}

    .slick-list {
     position: relative; 
     display: block; 
     overflow: hidden; 
     margin: 0; 
    padding: 0;
}
}   
.em{
    font-style: italic;
     font-size: 0.8em ;   
    text-transform: uppercase;
   margin-right:200px;
   
}
.upper{
        font-family: "BarlowCondensed",sans-serif;
    font-size: 50px;
    font-weight: 700;
    line-height: .8;
    position: relative;
    display: block;
    text-transform: uppercase;
 
}
.lower{
  font-size: 0.8em ;   
  text-transform: uppercase;
   margin-right:350px;
  
   

}
</style>