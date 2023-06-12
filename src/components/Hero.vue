<template>
  <div>
    <b-carousel
      id="carousel-1"
      v-model="slide"
      :interval="4000"
      controls
      indicators
      background="#ababab"
      img-width="1024"
      img-height="480"
      style="text-shadow: 1px 1px 2px #333;"
      @sliding-start="onSlideStart"
      @sliding-end="onSlideEnd"
    >
    

      <!-- Slides with custom text -->
      <b-carousel-slide img-src="https://static.tvmaze.com/uploads/images/original_untouched/1/3177.jpg">
        <h1>Garden of Bones</h1>
 <span class="fa fa-star checked"></span>
      <span class="fa fa-star checked"> </span>
      <span class="fa fa-star checked"> </span>
      <span class="fa fa-star checked"> </span><br><br> 
         <button class="btn btn-warning  ">WATCH NOW</button>
      </b-carousel-slide>

       <b-carousel-slide img-src="https://static.tvmaze.com/uploads/images/original_untouched/1/2668.jpg">
        <h1>The Ghost of Harrenhal</h1>
 <span class="fa fa-star checked"></span>
      <span class="fa fa-star checked"> </span>
      <span class="fa fa-star checked"> </span>
      <span class="fa fa-star checked"> </span><br><br>
        <button class="btn btn-warning  ">WATCH NOW</button>
      </b-carousel-slide>

       <b-carousel-slide img-src="https://static.tvmaze.com/uploads/images/original_untouched/1/3180.jpg">
       <h1>The Old Gods</h1>
 <span class="fa fa-star checked"></span>
      <span class="fa fa-star checked"> </span>
      <span class="fa fa-star checked"> </span>
      <span class="fa fa-star checked"> </span><br><br>
        <button class="btn btn-warning  ">WATCH NOW</button>
      </b-carousel-slide>

     
    </b-carousel>

  
  </div>
</template>

<script>
export default {
  name: "Hero",
  props: ["product"],
};

</script>





