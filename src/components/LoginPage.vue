<template>
<body>
<div class="container pt-4 pb-5">
    <div class="text-1"></div>
    <div class="text-2"></div>
    <div class="text-3"></div>
    <form action="" >
        <div class="text-center pt-3">
            
            <p class="display-7 fw-bold">Log<span class="ps-1">In</span></p> <small class="d-flex align-items-center justify-content-center mb-3">
                
                <p class="text-muted"> You don't  have an account?</p>
                <a class="btn btn-primary" href="#/signup">sign Up </a>
            </small>
        </div>
        <div class="row px-md-4 px-1 m-0 needs-validation" novalidate>
            <div class="col-12">
                <div>
                    <p for="validationCustom01" class="pb-1 username"   >Username</p>   
                                            
                        <input type="text" class="form-control" id="validationCustom01"  required>
                    
                </div>
            </div>
           
            <div class="col-12" for="validationCustom02" > <input type="password" class="form-control" id="validationCustom02"  placeholder="Password " required> </div>
            <div class="col-12 create">
                    <div class="d-flex align-items-center justify-content-between"   >
                          <button type="submit"  class="btn btn-primary  btn btn-primary py-3">Login</button>   
                </div>
                <small class=" text-center pt-3 d-flex align-items-center justify-content-center mb-3">
                
                <p class="text-muted">Or Login With </p>
                <a class="v d-flex align-items-center justify-content-center mb-3" href="#/forgot">  Forgot the password </a>
            </small>
             <div class="row mx-auto  ">
                    <div class="col-4"> <i class="fab fa-twitter"></i> </div>
                    <div class="col-4"> <i class="fab fa-facebook"></i> </div>
                    <div class="col-4"> <i class="fab fa-google"></i> </div>
                    </div>
            </div>
        </div>
        
    </form>
</div>
</body>
</template>

<script>
export default {
  name: 'LoginPage',
  props: {
    msg: String
  },

  function () {
  'use strict'

  // Fetch all the forms we want to apply custom Bootstrap validation styles to
  var forms = document.querySelectorAll('.needs-validation')

  // Loop over them and prevent submission
  Array.prototype.slice.call(forms)
    .forEach(function (form) {
      form.addEventListener('submit', function (event) {
        if (!form.checkValidity()) {
          event.preventDefault()
          event.stopPropagation()
        }

        form.classList.add('was-validated')
      }, false)
    })
  }

}
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css?family=Montserrat:400,700&display=swap');
.fa-twitter {
    color: #56ABEC
}

.fa-facebook {
    color: #1775F1
}

.fa-google {
    color: #CB5048
}
.fab {
    display: flex;
    justify-content: center;
    align-items: center;
    border: none;
    background: #2A284D;
    height: 40px;
    width: 90px
}
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    list-style: none;
    font-family: 'Montserrat', sans-serif
}

p {
    margin: 0px
}

body {
    display: flex;
    justify-content: center;
    align-items: center;
    min-height: 100vh;
    background-image: url(E:\pet-vue\src\assets\forest-stream-shenandoah-national-park-justin-black-iLCP-1171x593.jpg );
    background-repeat: no-repeat;
     background-size: cover;
    padding: 30px 10px
}

.container {
    max-width: 500px;
    background-color: #010152;
    margin: auto;
    color: white;
    border-radius: 10px;
    position: relative
}

.text-1 {
    position: absolute;
    top: -50px;
    left: -30%;
    width: 350px;
    height: 350px;
    clip-path: circle(50%);
    background-color: #2d4dda;
    z-index: -1
}

.text-2 {
    position: absolute;
    top: -30px;
    right: -10%;
    width: 100px;
    height: 100px;
    clip-path: circle(50%);
    background-color: #2d4dda
}

.text-3 {
    position: absolute;
    bottom: -50px;
    right: -10%;
    width: 150px;
    height: 150px;
    clip-path: circle(50%);
    background-color: #2d4dda;
    z-index: -1
}

.display-7 {
    font-size: 35px
}

small .btn.btn-primary {
    background-color: transparent;
    border: none;
    color: #26D0CE
}

.create .btn.btn-primary {
    width: 100%;
    padding: 0 20px;
    display: block;
    color: white;
    font-size: 14px;
    font-weight: 600;
    background-image: linear-gradient(to right, #1A2980 0%, #26D0CE 51%, #1A2980 100%);
    background-size: 200% auto;
    border: none;
    text-transform: capitalize;
    transition: 0.5s
}

.create .btn.btn-primary:hover {
    background-position: right center;
    color: #fff;
    text-decoration: none
}

.create .btn.btn-primary:hover .fas {
    transform: translateX(10px);
    transition: transform 0.5s ease
}

.form-control {
    color: white;
    text-transform: capitalize;
    background-color: #060672;
    border: 2px solid transparent;
    height: 50px;
    padding-left: 20px
}

.form-control:focus {
    color: white;
    background-color: #010152;
    border: 2px solid #2d4dda;
    box-shadow: none
}

.username {
    font-size: 14px
}

::placeholder {
    font-size: 12px;
    font-weight: 600    
}

@media(max-width:930px) {
    .text-1 {
        display: none
    }

    .text-2 {
        z-index: -1
    }

    .display-7 {
        font-size: 30px
    }
}
</style>