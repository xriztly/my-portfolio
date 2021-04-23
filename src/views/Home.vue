<template>
  <div class="home">
    
   <v-carousel >
      <v-carousel-item
        v-for="(item,i) in items"
        :key="i"
        :src="item.src"
      ></v-carousel-item>
    </v-carousel>

    <div id="style">
      <span>Lorem ipsum dolor sit amet consectetur adipisicing elit. Eveniet sed error accusantium soluta iste, fugit nam deserunt sit fuga dignissimos asperiores illum incidunt, iure voluptatem quae qui! Obcaecati, accusantium aut!</span>
    </div>
  </div>

  
</template>

<script>
// @ is an alias to /src

export default {
 data () {
    return {
      items: [
        {
          src: 'https://cdn.vuetifyjs.com/images/carousel/squirrel.jpg',
        },
       
      ],
    }
  },

 
}

  
</script>


<style scoped>
#style{
 width:100%;
 height: 100px;
 background-color: grey;
}
</style>