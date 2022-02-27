<template>
<div  class="footer back2 ">
  <div class="inner-context ">
      <table style=" margin-top:20px " >
          <tr  style=" margin-top:20px " >
              <td style=" margin-top:20px " >
                  <a  href="#/login" style=" margin-top:20px " >
      <img    src="https://img.freepik.com/free-vector/pet-shop-paw-logo_142351-10.jpg" width="300" height="200"/>
    </a>
    <div> <h3 class="sub" >Subcribe to our newsletter</h3>
        <table><tr>
            <td ><input style=" margin-top:40px "  type="email"  required placeholder="example@gmail.com"></td>
            <td> 
                <form class="d-flex">
        <button type="button"  style=" margin-top:40px "  class="btn btn-outline-danger">Subcribe</button>
      </form>
            </td>
            </tr></table>

            

    </div>
    
    <div> 
        <ul style="margin-top: 5px">
            <li><i class="bi bi-facebook"></i></li>
            <li><i class="bi bi-instagram"></i></li>
            <li><i class="bi bi-envelope-open"></i></li>
            <li><i class="bi bi-youtube"></i></li>
        </ul>
    </div>
              </td>
                
              <td class="tit">
                  <h3 class="city" >HaNoi</h3>
                  <p>Hotline: 1900 234567</p>
                  <p>Email: info@g  dinamodpet.vn</p>
                  <p>Opening hours: 9 am- 7 pm (7 days)</p>
                  <p>24/7 emergency and critical care</p>
                   <h3 class="city" style="padding-top: 50px" >Da Nang</h3>
                  <p>Hotline: 1900 765432</p>
                  <p>Email: info@gdinamodpet.vn</p>
                  <p>Opening hours: 9 am- 7 pm (7 days)</p>
                  <p>24/7 emergency and critical care</p>
              </td>
          </tr>
      </table>
  </div>
</div>
</template>

<script>
export default {
  name: 'FooterUser',
  props: {
    msg: String
  }
}
</script>

<style scoped>
.white{
    color: aliceblue;
}
.city{
    font-weight: 750;
    text-transform: uppercase;
}
.sub{
color: aliceblue;
}
.tit{
    font-family: "BarlowCondensed",sans-serif;
    font-weight: 750;
    line-height: 1.3;
    margin-bottom: 450px;
    color:aliceblue;
    padding-left : 600px
    
}
 .inner-context{
      margin-left: 80px;
      margin-top: 10px;

   
  }
  
  .footer{
  border:1px solid #000000;
  background-image: url(E:\pet-vue\src\assets\two-dogs.png);
  padding-top: 80px ;
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
  ;
}
</style>