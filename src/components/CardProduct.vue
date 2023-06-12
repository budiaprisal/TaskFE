<template>
  <div class="card shadow card-product ">
    <!-- <img :src=" 'assets/images/' + product.gambar " class="card-img-top" alt="..." /> -->
    <img
      :src="product.image.original"
      width="100%"
      height="100%"
      object-fit="cover"
      cursor="pointer"
    />
    <div class="card-body" object-fit="cover" cursor="pointer">
      <p class="card-text">Seasons {{ product.id }}</p>
      <span class="fa fa-star checked"></span>
      <span class="fa fa-star checked"> </span>
      <span class="fa fa-star checked"> </span>
      <span class="fa fa-star checked"> </span>
      <span class="fa fa-star"></span> <span></span>
      <span class="card-text">{{ product.rating.average }}</span> <br><br>

      <link
        rel="stylesheet"
        href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/4.7.0/css/font-awesome.min.css"
        />
      <router-link class="btn btn-warning" :to="'/foods/' + product.id"
        ><b-icon-info> </b-icon-info> More Info </router-link
      >
    </div>
  </div>

  
  
  
</template>


<script>
export default {
  name: "CardProduct",
  props: ["product"],
};
</script>

<style>


.checked {
  color: orange;
}

/* Three column layout */
.side {
  float: left;
  width: 15%;
  margin-top: 10px;
}

.middle {
  margin-top: 10px;
  float: left;
  width: 70%;
}

/* Place text to the right */
.right {
  text-align: right;
}

/* Clear floats after the columns */
.row:after {
  content: "";
  display: table;
  clear: both;
}

/* The bar container */
.bar-container {
  width: 100%;
  background-color: #f1f1f1;
  text-align: center;
  color: white;
}

/* Individual bars */
.bar-5 {
  width: 60%;
  height: 18px;
  background-color: #04aa6d;
}
.bar-4 {
  width: 30%;
  height: 18px;
  background-color: #2196f3;
}
.bar-3 {
  width: 10%;
  height: 18px;
  background-color: #00bcd4;
}
.bar-2 {
  width: 4%;
  height: 18px;
  background-color: #ff9800;
}
.bar-1 {
  width: 15%;
  height: 18px;
  background-color: #f44336;
}

/* Responsive layout - make the columns stack on top of each other instead of next to each other */
@media (max-width: 400px) {
  .side,
  .middle {
    width: 100%;
  }
  .right {
    display: none;
  }
}
</style>
