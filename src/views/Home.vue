<template>
  <div class="home">
  
      <v-row 
     
   >
        <v-col cols="12">
          
            <v-img
              id="bg"
              height="400"
              class="text-center rounded-tl-xl rounded-br-xl"
                
            > 
            <v-row style="padding-top:100px"  
            align="center"
            justify="center">
              <v-col cols="8" class="text-center t" >
                 <h2 style="color:#243248; font-family:san-serif; ">Hi!, I'M XRIZT</h2>
              <h3 class="subheading" > 
                 <span class="grey--text">I AM  </span>
                 <span style="color:#51c4d3">VUEJS/VUETIFY</span>
                  <span class="grey--text"> DEVELOPER</span>
              </h3>
              </v-col>
            </v-row>
             
            </v-img>
     
        </v-col>
      </v-row>
  </div>

  
</template>

<script>
// @ is an alias to /src

export default {
 
}
</script>


<style scoped>
#bg{
  background-image: url('../assets/para.jpg');
 background-size:cover;
}
</style>