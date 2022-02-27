<template>
<div style="background-color: burlywood;"  >
  <div class="inner-context" >
      <h1 class="upper "> Our Blogs</h1>
      <hr style="width:15%;text-align:left;  color: red;">
     <table style="margin-top: 100px">
         <tr>
             <td>
                 <div class="card mar  id " >
                     <a style="nav-link active" href="#">
  <img src="https://www.theanimaldoctors.org/wp-content/uploads/2021/01/THUBNAIL.png" class="card-img-top one " >
  <h5 class="upper2    " >Osteoarthritis in dogs? Majority of OA in dog occur </h5></a>
  <div >
    
    <p class=" des" >Everything you need know about OSTEARTHRITIS in DOGs Osteoarthritis or Degenrative Joint  Disease (DJD) is a slow , ongoing.Majority of OA in dog occur secondarily to developmental orthopedic disease...</p>
    
  </div>
</div>
             </td>
             <td>
                 <div class="card mar id">
                     <a style="nav-link active" href="#">
  <img src="https://www.theanimaldoctors.org/wp-content/uploads/2020/11/87888707_1087753101560295_5830836026112737280_o.jpg" class="card-img-top one  " >
  <h5 class="upper2 nav-link active">Tick fever - is your dog protected? </h5>
  </a>
  <div class="card-body">
    
    <p class="des"> Tick Fever- Is your dog protected? Ticks live everwhere in Vietnam PDR and survive here all year round. ONE bite from ONE tick can...</p>
    
  </div>
</div>
             </td>
             <td>
                 <div class="card mar id">
                     <a style="nav-link active" href="#">
  <img src="https://www.theanimaldoctors.org/wp-content/uploads/2020/03/11.jpeg" class="card-img-top  one" >
                     <h5 class="upper2 nav-link active">The most common health problems </h5>
                     </a>
  <div class="card-body">
    <p class="des">The most common health problems in kittens and young cats in Vietnam internal parasites (worms) Roundworm, hookworm,tapeworm,giardia,...</p>
    
  </div>
</div>
             </td>
         </tr>
     </table>


  </div>
  </div>
</template>

<script>
export default {
  name: 'OurBlogUser',
  props: {
    msg: String
  }
}
</script>

<style scoped>
.mar{
 margin-left: 0px ;
 background-color: aliceblue;
}
.id{
  width: 20rem;
   margin-left : 70px ;
   margin-bottom: 50px;

}
h5:hover{
background-color: whitesmoke;
  color: red;
}

.upper2{
     width: 100%;
    max-height: 87px;
    height: auto;
    
    overflow: hidden;
    text-overflow: ellipsis;
    -webkit-line-clamp: 4;
    -webkit-box-orient: vertical;
    display: -webkit-box;
    display: -moz-box;
    display: -ms-flexbox;
}
.des{
    width: 100%;
    max-height: 87px;
    height: auto;
    overflow: hidden;
    text-overflow: ellipsis;
    -webkit-line-clamp: 4;
    -webkit-box-orient: vertical;
    display: -webkit-box;
    display: -moz-box;
    display: -ms-flexbox;
}
 .one{
     height: 200px;
    
 }
 .upper2 {
    font-family: "BarlowCondensed",sans-serif;
    margin-top: 10px;
    font-size: 23px;
    font-weight: 700;
    line-height: .8;
    position: relative;
    display: block;
    text-transform: uppercase;
}
 .des{
  font-weight: 700;
    letter-spacing: -.1px;
    color: #2d231a;
    
 }
.news_item .news_item-image {
    height: 218px;
    background-repeat: no-repeat;
    background-position: center center;
    background-size: cover;
}
  .inner-context{
      margin-left: 150px;
   
   
  }
</style>