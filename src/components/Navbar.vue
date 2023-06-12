<template>
  <div>
    <b-navbar toggleable="lg" type="light">
      <div class="container">
        <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>

        <b-collapse id="nav-collapse" is-nav>
          <div class="navbar-nav">
            <a>
              <router-link class="nav-link" to="/">Home</router-link>
            </a>
            <a>
              <router-link class="nav-link" to="/foods"
                >Game Of Trones</router-link
              >
            </a>
          </div>

          <!-- Right aligned nav items -->
          <b-navbar-nav class="ml-auto navbar-ekstra">
            <a href="#" id="search"><i data-feather="search"></i> </a>
          </b-navbar-nav>
        </b-collapse>
      </div>
    </b-navbar>
  </div>
</template>

<script>
import axios from "axios";

export default {
  name: "Navbar",
  data() {
    return {
      jumlah_pesanans: [],
    };
  },
  props: ["updateKeranjang"],
  methods: {
    setJumlah(data) {
      this.jumlah_pesanans = data;
    },
  },
  mounted() {
    axios
      .get("http://localhost:3000/keranjangs")
      .then((response) => this.setJumlah(response.data))
      .catch((error) => console.log(error));
  },
};
</script>

<style>
*{
  margin:0;
  padding:0;
  box-sizing: border-box;
  outline: none;
  text-decoration: none;
}

.navbar .navbar-nav a{
  color: rgb(202, 236, 66);
  display: inline-block;
  font-size: 1.3rem;
  margin:0  1rem;
  
}

.navbar .navbar-nav a:hover {
  color: yellow;

}

.navbar .navbar-nav a::after {
  content: '';
  display: block;
  border-bottom: 0.1rem solid var(--yellow);
  transform: scaleX(0);
  transition: 0.2s linear;
 
}

.navbar .navbar-nav a:hover::after{
  transform: scaleX(1);
}




</style>
