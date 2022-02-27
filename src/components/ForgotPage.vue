<template>
<body>
<div class="container pt-4 pb-5">
    <div class="text-1"></div>
    <div class="text-2"></div>
    <div class="text-3"></div>
    <form action="">
         <div class="form-data" v-if="!submitted">
        <div class="text-center pt-3">
            <p class="display-7 fw-bold">Forgot<span class="ps-1">Password</span></p> 
                <p class="text-center pt-3" >1. Enter your email address below.</p>
                <p class="text-center pt-3" > 2. Our system will send you a temporary link</p>
                <p  class="text-center pt-3">3. Use the link to reset your password</p>
             <div>
                    <div class="col-12">Email</div> <input type="text" v-model="email" placeholder="example@gmail.com" v-bind:class="{'form-control':true, 'is-invalid' : !validEmail(email) && emailBlured}" v-on:blur="emailBlured = true">
                        <div class="invalid-feedback">A valid email is required!</div>
            </div> <small class="d-flex align-items-center justify-content-center mb-3">
                    <div class="col-7 create d-flex align-items-center justify-content-center">
                        <button type="submit"  class="btn btn-primary btn btn-primary py-3 ">Reset Password</button> <span class="fas fa-arrow-right "></span>                
                </div> </small> <small class="d-flex align-items-center justify-content-center mb-7">
                    <div class="col-4 create d-flex align-items-center justify-content-between">
                        <a  href="#/login" class="btn btn-primary btn btn-primary py-2 ">Back to login</a> <span class="fas fa-arrow-right "></span>                
                </div>
                </small>
                
            </div>
        </div>
    </form>
</div>
</body>
</template>

<script>
export default {
  name: 'ForgotPage',
  props: {
    msg: String
  },
  data: function () {
return {
email : "",
emailBlured : false,
valid : false,
submitted : false,
password:"",
passwordBlured:false,
username:"",
usernameBlured:false,
phone:"",
phoneBlured:false
}
},
 methods:{

validate : function(){
this.emailBlured = true;
this.passwordBlured = true;
this.usernameBlured = true;
this.phoneBlured = true;
if( this.validEmail(this.email) && this.validPassword(this.password) && this.validPhone(this.phone) && this.validUsername(this.username)){
this.valid = true;
}
},

validEmail : function(email) {
var re = /(.+)@(.+){2,}\.(.+){2,}/;
if(re.test(email.toLowerCase())){
return true;
}
},

validPassword : function(password) {
if (password.length > 7) {
return true;
}
},

validUsername : function(username) {

if (!/\s/.test(username)) {
return true;
}
},
validPhone : function(phone) {
if (phone.length > 9 && phone.length < 12 ) { return true; } },
 submit : function()
 { this.validate(); if(this.valid){ this.submitted=true; } } }, }

</script>

<style scoped>
@import url('https://fonts.googleapis.com/css?family=Montserrat:400,700&display=swap');

.forms-inputs {
    position: relative
}
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
.forms-inputs span {
    position: absolute;
    top: -18px;
    left: 10px;
    background-color: #fff;
    padding: 5px 10px;
    font-size: 15px
}

.forms-inputs input {
    height: 50px;
    border: 2px solid #eee
}

.forms-inputs input:focus {
    box-shadow: none;
    outline: none;
    border: 2px solid #000
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
    background-image: url(E:\pet-vue\src\assets\Raising-a-Happy-Dog-7-768x512.jpg );
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