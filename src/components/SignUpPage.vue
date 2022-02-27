<template>
  <body>
    <div class="container pt-4 pb-5">
      <div class="text-1"></div>
      <div class="text-2"></div>
      <div class="text-3"></div>
      <form id="form1">
        <div class="form-data" v-if="!submitted">
          <div class="text-center pt-3">
            <p class="display-7 fw-bold">
              Create<span class="ps-1">account</span>
            </p>
            <small
              class="d-flex align-items-center justify-content-center mb-3"
            >
              <p class="text-muted">Already have an account?</p>
              <a class="btn btn-primary" href="#/login">sign in</a>
            </small>
          </div>
          <div class="row px-md-4 px-1 m-0">
            <div class="col-12">
              <div>
                <div class="col-12">Email</div>
                <input
                  type="text"
                  v-model="email"
                  v-bind:class="{
                    'form-control': true,
                    'is-invalid': !validEmail(email) && emailBlured,
                  }"
                  v-on:blur="emailBlured = true"
                />
                <div class="invalid-feedback">A valid email is required!</div>
              </div>
              <div class="col-12">
                <input
                  type="text"
                  v-model="phone"
                  v-bind:class="{
                    'form-control': true,
                    'is-invalid': !validPhone(phone) && phoneBlured,
                  }"
                  v-on:blur="phoneBlured = true"
                />
                <div class="invalid-feedback">A valid phone is required!</div>
                <div class="pb-1 username">
                  <input
                    type="text"
                    v-model="username"
                    v-bind:class="{
                      'form-control': true,
                      'is-invalid': !validUsername(username) && usernameBlured,
                    }"
                    v-on:blur="usernameBlured = true"
                  />
                  <div class="invalid-feedback">
                    A valid username is required!
                  </div>
                  <div></div>
                  <div class="col-12">
                    <input
                      type="password"
                      v-model="password"
                      v-bind:class="{
                        'form-control': true,
                        'is-invalid':
                          !validPassword(password) && passwordBlured,
                      }"
                      v-on:blur="passwordBlured = true"
                    />
                    <div class="invalid-feedback">
                      Password must be 8 character!
                    </div>
                    <div class="col-12 create">
                      <input
                        class="form-check-input"
                        type="checkbox"
                        value=""
                        id="flexCheckDefault"
                        required
                        v-model="terms"
                      />
                      <label class="form-check-label" for="flexCheckDefault">
                        Accept term and conditions
                      </label>

                      <div
                        class="
                          d-flex
                          align-items-center
                          justify-content-between
                        "
                      >
                        <button
                          type="submit"
                          class="btn btn-primary btn btn-primary py-3"
                        >
                          Create Your Account
                        </button>
                        <span class="fas fa-arrow-right"></span>
                      </div>

                      <div class="row mx-auto">
                        <div class="col-4"><i class="fab fa-twitter"></i></div>
                        <div class="col-4"><i class="fab fa-facebook"></i></div>
                        <div class="col-4"><i class="fab fa-google"></i></div>
                      </div>
                    </div>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </form>
    </div>
  </body>
</template>

<script>
export default {
  name: "SignUpPage",
  props: {
    msg: String,
  },
  data: function () {
    return {
      email: "",
      emailBlured: false,
      valid: false,
      submitted: false,
      password: "",
      passwordBlured: false,
      username: "",
      usernameBlured: false,
      phone: "",
      phoneBlured: false,
    };
  },
  methods: {
    validate: function () {
      this.emailBlured = true;
      this.passwordBlured = true;
      this.usernameBlured = true;
      this.phoneBlured = true;
      if (
        this.validEmail(this.email) &&
        this.validPassword(this.password) &&
        this.validPhone(this.phone) &&
        this.validUsername(this.username)
      ) {
        this.valid = true;
      }
    },

    validEmail: function (email) {
      var re = /(.+)@(.+){2,}\.(.+){2,}/;
      if (re.test(email.toLowerCase())) {
        return true;
      }
    },

    validPassword: function (password) {
      if (password.length > 7) {
        return true;
      }
    },

    validUsername: function (username) {
      if (!/\s/.test(username)) {
        return true;
      }
    },
    validPhone: function (phone) {
      if (phone.length > 9 && phone.length < 12) {
        return true;
      }
    },
    submit: function () {
      this.validate();
      if (this.valid) {
        this.submitted = true;
      }
    },
  },
};
</script>

<style scoped>
@import url("https://fonts.googleapis.com/css?family=Montserrat:400,700&display=swap");

.forms-inputs {
  position: relative;
}
.fa-twitter {
  color: #56abec;
}

.fa-facebook {
  color: #1775f1;
}

.fa-google {
  color: #cb5048;
}
.fab {
  display: flex;
  justify-content: center;
  align-items: center;
  border: none;
  background: #2a284d;
  height: 40px;
  width: 90px;
}
.forms-inputs span {
  position: absolute;
  top: -18px;
  left: 10px;
  background-color: #fff;
  padding: 5px 10px;
  font-size: 15px;
}

.forms-inputs input {
  height: 50px;
  border: 2px solid #eee;
}

.forms-inputs input:focus {
  box-shadow: none;
  outline: none;
  border: 2px solid #000;
}
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  list-style: none;
  font-family: "Montserrat", sans-serif;
}

p {
  margin: 0px;
}

body {
  display: flex;
  justify-content: center;
  align-items: center;
  min-height: 100vh;
  background-image: url(E:\pet-vue\src\assets\Raising-a-Happy-Dog-7-768x512.jpg);
  background-repeat: no-repeat;
  background-size: cover;
  padding: 30px 10px;
}

.container {
  max-width: 500px;
  background-color: #010152;
  margin: auto;
  color: white;
  border-radius: 10px;
  position: relative;
}

.text-1 {
  position: absolute;
  top: -50px;
  left: -30%;
  width: 350px;
  height: 350px;
  clip-path: circle(50%);
  background-color: #2d4dda;
  z-index: -1;
}

.text-2 {
  position: absolute;
  top: -30px;
  right: -10%;
  width: 100px;
  height: 100px;
  clip-path: circle(50%);
  background-color: #2d4dda;
}

.text-3 {
  position: absolute;
  bottom: -50px;
  right: -10%;
  width: 150px;
  height: 150px;
  clip-path: circle(50%);
  background-color: #2d4dda;
  z-index: -1;
}

.display-7 {
  font-size: 35px;
}

small .btn.btn-primary {
  background-color: transparent;
  border: none;
  color: #26d0ce;
}

.create .btn.btn-primary {
  width: 100%;
  padding: 0 20px;
  display: block;
  color: white;
  font-size: 14px;
  font-weight: 600;
  background-image: linear-gradient(
    to right,
    #1a2980 0%,
    #26d0ce 51%,
    #1a2980 100%
  );
  background-size: 200% auto;
  border: none;
  text-transform: capitalize;
  transition: 0.5s;
}

.create .btn.btn-primary:hover {
  background-position: right center;
  color: #fff;
  text-decoration: none;
}

.create .btn.btn-primary:hover .fas {
  transform: translateX(10px);
  transition: transform 0.5s ease;
}

.form-control {
  color: white;
  text-transform: capitalize;
  background-color: #060672;
  border: 2px solid transparent;
  height: 50px;
  padding-left: 20px;
}

.form-control:focus {
  color: white;
  background-color: #010152;
  border: 2px solid #2d4dda;
  box-shadow: none;
}

.username {
  font-size: 14px;
}

::placeholder {
  font-size: 12px;
  font-weight: 600;
}

@media (max-width: 930px) {
  .text-1 {
    display: none;
  }

  .text-2 {
    z-index: -1;
  }

  .display-7 {
    font-size: 30px;
  }
}
</style>