<template>
 <div id="container">
    
    <v-app-bar
      app
      flat
     class="#080808 grey--text"
      dark
    >
      <v-app-bar-nav-icon class="hidden-md-and-up grey--text" @click.stop="drawer=!drawer"></v-app-bar-nav-icon>

      <div class="d-flex align-center">
        
       <v-toolbar-title class="text-uppercase" >
        <span style="color:#51c4d3; ">Developer</span>
        <span style="color:#51c4d3; opacity: 80%;">mode  </span>
       </v-toolbar-title>
        
      </div>

      <v-spacer></v-spacer>

      <v-btn
        class="hidden-sm-and-down "
        text
       v-for="link in links"
       :key="link.title"
       route :to="link.route"

      >
        <span class="mr-2 " style="color:#51c4d3; opacity: 80%; " >{{link.title}}</span>
      </v-btn>
    </v-app-bar>

<!-- for navigation drawer-->
         <v-navigation-drawer style="background-color:#272727;"
      v-model="drawer"
      fixed
      side
      temporary
    >
  <template v-slot:prepend>
        <v-list-item two-line>
          <v-list-item-avatar>
            <img src="@/assets/logo.png">
          </v-list-item-avatar>

          <v-list-item-content  >
            <v-list-item-title id="name">Christly Tejano</v-list-item-title>
                  <v-list-item-subtitle id="edit" >Vuejs/Vuetify</v-list-item-subtitle>
                        <v-list-item-subtitle id="edit">Developer</v-list-item-subtitle>
          </v-list-item-content>
        </v-list-item>
      </template>

<v-divider style="background-color:#51c4d3;"></v-divider>

      <v-list
        nav
        dense
      >
        <v-list-item-group
         
        >
          <v-list-item 
          v-for="item in links"
          :key="item.title"
          route :to="item.route"
          >
            <v-list-item-title style="color:#51c4d3; opacity: 80%;">{{item.title}}</v-list-item-title>
          </v-list-item>

         
        </v-list-item-group>
      </v-list>
    </v-navigation-drawer>
   


 </div>

 
</template>

<script>


export default {
  name: 'App',

  components: {
    
  },

  data() {
    return {
        
        drawer: false,
        group: null,
        links:[
         { title: 'Home', icon: 'mdi-view-dashboard', route:'/'},
          { title: 'About', icon: 'mdi-gavel', route:'/About' },
          { title: 'Skill', icon: 'mdi-gavel', route:'/Skill' },
          { title: 'Contact', icon: 'mdi-gavel', route:'/Contact'},
         
        ],
       
      }
      
  },
};
</script>

<style scoped>
#container{
  background-image: url("/assets/bg.jpg");

}
#edit{
 color:#51c4d3;
}
#name{
  color:#d8e3e7;
  font-size: 25px;
  font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
}

</style>

