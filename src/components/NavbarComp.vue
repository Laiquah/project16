<template>
  <div>
    <nav class="navbar navbar-expand-lg">
      <div class="container-fluid">
        <a class="navbar-brand" href="../views/HomeView.vue"
          ><img src="" alt="logo" loading="lazy"
        /></a>
        <button
          class="navbar-toggler"
          type="button"
          data-bs-toggle="collapse"
          data-bs-target="#navbarSupportedContent"
          aria-controls="navbarSupportedContent"
          aria-expanded="false"
          aria-label="Toggle navigation"
        >
          <span class="navbar-toggler-icon"></span>
        </button>
        <div class="collapse navbar-collapse" id="navbarSupportedContent">
          <ul class="navbar-nav m-auto mb-2 mb-lg-0">
            <li class="nav-item">
              <router-link to="/">home</router-link>
            </li>
            <li class="nav-item">
              <router-link to="/game">game</router-link>
            </li>
            <li class="nav-item">
              <router-link to="/about">about</router-link>
            </li>
            <li class="nav-item">
              <router-link to="/help">help</router-link>
            </li>
          </ul>
        </div>
      </div>
      <button
        type="button"
        class="btn"
        id=""
        data-bs-toggle="modal"
        data-bs-target="#exampleModal"
      >
        Sign up
      </button>

      <div
        class="modal fade"
        id="exampleModal"
        tabindex="-1"
        aria-labelledby="exampleModalLabel"
        aria-hidden="true"
      >
        <div class="modal-dialog">
          <div class="modal-content">
            <div class="modal-header">
              <button
                type="button"
                class="btn-close"
                data-bs-dismiss="modal"
                aria-label="Close"
              ></button>
            </div>
            <div class="modal-body">
              <form class="form">
                <p class="title">Sign up here</p>
                <p class="message">
                  Signup now and get full access to our web page.
                </p>
                <div class="flex">
                  <label>
                    <input
                      required="name"
                      placeholder=""
                      type="text"
                      class="input"
                    />
                    <span>Firstname</span>
                  </label>

                  <label>
                    <input
                      required="name"
                      placeholder=""
                      type="text"
                      class="input"
                    />
                    <span>Lastname</span>
                  </label>
                </div>

                <label>
                  <input
                    required="email"
                    placeholder=""
                    type="email"
                    class="input"
                  />
                  <span>Email</span>
                </label>

                <label>
                  <input
                    required="password"
                    placeholder=""
                    type="password"
                    class="input"
                  />
                  <span>Password</span>
                </label>
                <label>
                  <input
                    required=""
                    placeholder=""
                    type="password"
                    class="input"
                  />
                  <span>Confirm password</span>
                </label>
                <button class="submit">Submit</button>
                <p class="signin">
                  Already have an acount ? <a href="#">Signin</a>
                </p>
              </form>
            </div>
          </div>
        </div>
      </div>
    </nav>
  </div>
</template>

<script>
export default {};
</script>

<style scoped>
nav {
  background-color: #7895b2;
}
.nav-item {
  margin-left: 2rem;
  text-decoration: none;
  color: #f5efe6;
}

.form {
  display: flex;
  flex-direction: column;
  gap: 10px;
  background-color: #fff;
  padding: 20px;
  border-radius: 20px;
  position: relative;
}

.title {
  font-size: 28px;
  color: black;
  font-weight: 600;
  letter-spacing: -1px;
  position: relative;
  display: flex;
  text-align: center;
  align-items: center;
  padding-left: 30px;
}

.title::before,
.title::after {
  position: absolute;
  content: "";
  height: 16px;
  width: 16px;
  border-radius: 50%;
  left: 0px;
  background-color: royalblue;
}

.title::before {
  width: 18px;
  height: 18px;
  background-color: royalblue;
}

.title::after {
  width: 18px;
  height: 18px;
  animation: pulse 1s linear infinite;
}

.message,
.signin {
  color: rgba(88, 87, 87, 0.822);
  font-size: 14px;
}

.signin {
  text-align: center;
}

.signin a {
  color: royalblue;
}

.signin a:hover {
  text-decoration: underline royalblue;
}

.flex {
  display: flex;
  width: 100%;
  gap: 6px;
}

.form label {
  position: relative;
}

.form label .input {
  width: 100%;
  padding: 10px 10px 20px 10px;
  outline: 0;
  border: 1px solid rgba(105, 105, 105, 0.397);
  border-radius: 10px;
}

.form label .input + span {
  position: absolute;
  left: 10px;
  top: 15px;
  color: grey;
  font-size: 0.9em;
  cursor: text;
  transition: 0.3s ease;
}

.form label .input:placeholder-shown + span {
  top: 15px;
  font-size: 0.9em;
}

.form label .input:focus + span,
.form label .input:valid + span {
  top: 30px;
  font-size: 0.7em;
  font-weight: 600;
}

.form label .input:valid + span {
  color: green;
}

.submit {
  border: none;
  outline: none;
  background-color: royalblue;
  padding: 10px;
  border-radius: 10px;
  color: #fff;
  font-size: 16px;
  transform: 0.3s ease;
}

.submit:hover {
  background-color: rgb(56, 90, 194);
}

@keyframes pulse {
  from {
    transform: scale(0.9);
    opacity: 1;
  }

  to {
    transform: scale(1.8);
    opacity: 0;
  }
}

.btn {
  font-size: 18px;
  letter-spacing: 2px;
  text-transform: uppercase;
  display: inline-block;
  text-align: center;
  font-weight: bold;
  padding: 0.7em 2em;
  margin-right: 1rem;
  width: 10rem;
  border: 3px solid #7895b2;
  border-radius: 4rem;
  position: relative;
  box-shadow: 0 2px 10px rgba(0, 0, 0, 0.16), 0 3px 6px rgba(0, 0, 0, 0.1);
  color: white;
  text-decoration: none;
  transition: 0.3s ease all;
  z-index: 1;
}

.btn:before {
  transition: 0.5s all ease;
  position: absolute;
  top: 0;
  left: 50%;
  right: 50%;
  bottom: 0;
  opacity: 0;
  content: "";
  border-radius: 4rem;
  background-color: #aebdca;
  z-index: -1;
}

.btn:hover,
button:focus {
  color: white;
}

.btn:hover:before,
button:focus:before {
  transition: 0.5s all ease;
  left: 0;
  right: 0;
  opacity: 1;
}

.btn:active {
  transform: scale(0.9);
}
</style>
