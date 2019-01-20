<template>
<div>
<b-carousel id="carousel1"
                controls
                background="#ababab"
                :interval="5000"
                img-width="100%"
    >
      <!-- Text slides with image -->
      <b-carousel-slide>
        <img slot="img" class="d-block img-fluid w-100" width="1024" height="480"
             src="../assets/Tokyo-Ghoul---re.jpg" alt="image slot">
      </b-carousel-slide>
      <b-carousel-slide>
        <img slot="img" class="d-block img-fluid w-100" width="1024" height="480"
             src="..\assets\The-Seven-Deadly-Sins---Revival-of-The-Commandments.jpg" alt="image slot">
      </b-carousel-slide>
      <b-carousel-slide>
        <img slot="img" class="d-block img-fluid w-100" width="1024" height="480"
             src="..\assets\Steins-Gate-0.gif" alt="image slot">
      </b-carousel-slide>
      <b-carousel-slide>
        <img slot="img" class="d-block img-fluid w-100" width="1024" height="480"
             src="..\assets\Overlord-3rd-Season.jpg" alt="image slot">
      </b-carousel-slide>
       <b-carousel-slide>
        <img slot="img" class="d-block img-fluid w-100" width="1024" height="480"
             src="..\assets\How-NOT-to-Summon-a-Demon-Lord.jpg" alt="image slot">
      </b-carousel-slide>
       <b-carousel-slide>
        <img slot="img" class="d-block img-fluid w-100" width="1024" height="480"
             src="..\assets\Black-Clover.jpg" alt="image slot">
      </b-carousel-slide>
        <b-carousel-slide>
        <img slot="img" class="d-block img-fluid w-100" width="1024" height="480"
             src="..\assets\Attack-on-Titan-3.jpg" alt="image slot">
      </b-carousel-slide>
    </b-carousel>
    <div id="bdr"></div>
</div>
</template>

<script>
  export default {
     
  }
</script>

<style scoped>
div#bdr{
  border:1px solid black
}
</style> 