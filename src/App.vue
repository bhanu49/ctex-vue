<template>

<div id="app">
<div class="row topbar">
  <div class="col-md-9">

  </div>
  <div class="col-md-3 justify-content-center">
      <ul class="topbar-ele">
        <li class="">
            <router-link to="/register" class="" exact> Register</router-link>
          </li>
        <li class="">
            <router-link to="/sign-in" class="" exact> Sign In </router-link>
          </li>
      </ul>
  </div>
</div>
<div class="row">
    <nav class="navbar  navbar-expand-lg" v-bind:class="{ 'fixed-top': scrolled }">
        
        <div class="collapse navbar-collapse justify-content-center">
        <ul class="navbar-nav">
          <li class="nav-item ">
              <div class="logo">
                <span>Lo</span>go
              </div>
          </li>

          <li class="nav-item ">
            <router-link to="/" class="nav-link" exact>Home</router-link>
          </li>

          <li class="nav-item">
            <router-link to="/about" class="nav-link" exact>About</router-link>
          </li>

          <b-nav-item-dropdown text="Courses" left>
            <b-dropdown-item>
              <router-link to="/courses/all" exact> All </router-link>
            </b-dropdown-item>
            <b-dropdown-item>
              <router-link to="/students/cat 1" exact> Category 1 </router-link>
            </b-dropdown-item>
          </b-nav-item-dropdown>

          <li class="nav-item">
            <router-link to="/partners" class="nav-link" exact> Universities & Partners </router-link>
          </li> 

        </ul>
      </div>      
    
    </nav>
</div>

    <router-view/>
  </div>

</template>

<script>
export default {
 data () {
   return {
    scrolled: false
   };
  },
    methods: {
    handleScroll (e) {
      this.scrolled = true;
      console.log(e);
    }
  },
  created () {
   // window.addEventListener('scroll', this.handleScroll);
  }
}
</script>



<style lang="scss">
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
.logo{
  font-size: 25px;
  font-weight: bold;
}
.topbar{
  background:#d14a4a;

  ul{

    list-style-type: none;
   li{
    background: whitesmoke;
    float: left;
    padding: 10px;
    a{
      color: #4487cac0;
      text-decoration: none;
      font-weight: bold;
    }
    a:hover{
      color: #42b983;
    }
   }
  }
}
nav {
    width: 100%;
    background:whitesmoke;  
    transition: all 200ms ease;
    box-shadow: 0 1px 5px rgba(0, 0, 0, .25);
    backface-visibility: hidden;
  li{
    padding: 10px;
  }
  a {
    font-weight: bold;
    color: #2c3e50;
    font-size: 18px;
    &.router-link-exact-active {
      color: #42b983;
    }
  }
  a:hover{
    background-color: #dbdbdb;
    border-radius: 3%;
  }
}
</style>
