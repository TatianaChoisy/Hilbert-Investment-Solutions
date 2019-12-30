<template>

<div class="Navbar">

    <h2 class="logo">Hilbert Investment Solutions</h2>
    <input type="checkbox" id="chk">
    <label for="chk" class="show-menu-btn">
    <img alt="menu logo" class="menu-btn" src="../assets/menu.svg">
    </label>

    <ul class="menu">
      <a href="#Home">Home</a>
      <a href="#News">News</a>
      <a href="#Contact">Contact</a>
      <a href="#About">About</a>
      <label for="chk" class="hide-menu-btn">
      <img alt="menu close" class="menu-btn" src="../assets/close.svg">
      </label>

      <button class="btn">Sign In</button>
      <button class="btn sign-up">Sign Up</button>
    </ul>

</div>


</template>

<script>

export default {

  name: 'navbar'

}


</script>

<style scoped>

* {

  margin: 0;
  padding: 0;
  font-family: "Montserrat", sans-serif;
}

.Navbar {
  display: flex;
  justify-content: space-between;
  align-items: center;
  height: 100px;
  padding: 0 20px;
  background: #1e1e1e;
  color: #fff;
}

.logo {
  font-size: 20px;
  margin-left: 20px;
  line-height: 100px;
  float: left;

}

.menu-btn {

  height: 27px;
  width: 27px;
  float: right;
  line-height: 100px;
  margin-right: 40px;

}



.menu a {

  color: #fff;
  text-decoration: none;
  font-size: 16px;
  font-weight: 400;
  padding: 0 10px;
  transition: 0.4s;
  margin-right: 40px;

}


.show-menu-btn, .hide-menu-btn {

  transition: 0.4s;
  cursor: pointer;
  display: none;

}

.show-menu-btn {

  float: right;

}

.show-menu-btn i {

  line-height: 100px;
  
}

.menu a:hover, .show-menu-btn:hover, .hide-menu-btn:hover {

  color: #3498db;

}

#chk {

  position: absolute;
  visibility: hidden;
  z-index: -1111;

}

.btn {

  margin-left: 40px;
  background-color: #1e1e1e;
  border-color: #FFF;
  color: #FFF;
  font-size: 16px;
  width: 135px;
  height: 45px;
  cursor: pointer;

}

.sign-up {

  margin-right: 20px;

}

@media screen and (max-width:1250px) {
  .show-menu-btn, .hide-menu-btn {
    display: block;

  }

  .btn {

    display: none;

  }

  .menu {
    position: fixed;
    width: 100%;
    height: 100vh;
    background: #1e1e1e;
    right: -100%;
    top: 0;
    text-align: center;
    padding: 80px 0;
    line-height: normal;
    transition: 0.7s;
  }

  .menu a {
    display: block;
    padding: 20px;
    margin-right: 0px;
    font-size: 19px;
  }

  .hide-menu-btn {

    position: absolute;
    top: 40px;
    right: 40px;

  }

  #chk:checked ~ .menu {
    right: 0;
  }

}

</style>
