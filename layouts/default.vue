<template>
<v-app>

  <v-app-bar 
    app 
    clipped-left 
    height="110" 
    class="white pt-1" 
    elevation="1"
  >
    <v-col
      cols="12"
      class="white px-0 py-0"
    >
      <v-row>
        <v-app-bar-nav-icon @click.stop="drawer = !drawer"></v-app-bar-nav-icon>
        <a href="http://localhost:3000/">
          <v-img
            class="mt-4"
            height="20"
            width="100"
            :src="require('~/static/logo.png')"
            
          >
          </v-img>
        </a>
        <v-spacer class="d-none d-sm-flex"></v-spacer>

        <v-text-field 
            class = "search d-none d-lg-block"
            hide-details
            placeholder="Search"
            dense
            append-icon="mdi-magnify"
            solo
            outlined
        ></v-text-field> 

        <v-btn 
          light icon 
          class="mx-3 d-flex d-sm-none" 
          color="grey lighten-3" 
          fab small
        > 
          <v-icon color="black">mdi-magnify</v-icon> 
        </v-btn>

        <v-btn 
          class="mx-3 d-none d-lg-block" 
          color="grey lighten-3" 
          fab small
        > 
          <v-icon color="black">mdi-microphone</v-icon> 
        </v-btn>   

        <v-btn 
          light icon 
          class="mx-2 d-flex d-sm-none" 
          color="grey lighten-3" 
          fab small
        > 
          <v-icon color="black">mdi-microphone</v-icon> 
        </v-btn>   
        
        <v-btn 
          light icon 
          color="black" 
          class="mx-2" 
          fab small
        >
          <v-icon>mdi-apps</v-icon>
        </v-btn>
        <v-menu
          bottom
          left
        >
          <template v-slot:activator="{ on, attrs }">
            <v-btn
              light
              icon
              v-bind="attrs"
              v-on="on"
              class="mx-2"
              fab small
              color="black"
            >
              <v-icon>mdi-dots-vertical</v-icon>
            </v-btn>  
          </template>

          <v-list>
            <v-list-item
              v-for="item in items"
              :key="item.title"
              link
            >
              <v-list-item-title>{{item.icon}}</v-list-item-title>
              <v-list-item-title>{{item.title}}</v-list-item-title>
            </v-list-item>
          </v-list>
        </v-menu>
        <div class="text-centre pr-3 mx-0">
          <v-btn
            class="ma-0"
            outlined
            color="primary"
          >
            <v-icon>mdi-account</v-icon>  
            SIGN IN
          </v-btn>
        </div>  
      </v-row>
      <v-row class="pt-2"> 
        <v-divider></v-divider>
      </v-row>
      <v-row>
        <v-chip-group
          v-model="selection"
          active-class="black accent-4 white--text"
          column
          class="pl-2"
        >
          <v-chip>All</v-chip>
          <v-chip>Recently uploaded</v-chip>
          <v-chip>Watched</v-chip>
        </v-chip-group>
      </v-row>
    </v-col>
  </v-app-bar>
  
  <v-navigation-drawer
      class="d-none d-sm-flex"
      floating
      app
      clipped
      width="80px"
    >
      <v-list-item
        v-for="item in items"
        :key="item.title"
        link
        class="pa-0 pt-0"
      >
        <v-col class="pa-1 pt-0">
          <v-list-item-icon 
            class="ps-6 mb-0" 
            style="center"
          >  
            <v-icon>{{ item.icon }}</v-icon>  
          </v-list-item-icon>
          <v-list-item-title class="caption text-center">{{ item.title }}</v-list-item-title>
        </v-col>
      </v-list-item>
  </v-navigation-drawer>

  <v-navigation-drawer
    v-model="drawer"  
    temporary
    left
    app
  >  
    <v-list-item class="px-2">
      <v-list-item-content>        
        <v-list-item-title class="text-h6">
          <v-row class="pa-3"> 
            <v-app-bar-nav-icon light icon @click.stop="drawer = !drawer"></v-app-bar-nav-icon>
              <a href="http://localhost:3000/">
                <v-img
                  class="mt-3"
                  height="20"
                  width="100"
                  src="https://cdn.mos.cms.futurecdn.net/8gzcr6RpGStvZFA2qRt4v6-1024-80.jpg"
                >
                </v-img>
              </a>
          </v-row> 
        </v-list-item-title>
        
      </v-list-item-content>
    </v-list-item> 

    <v-list
      dense
    >
      <v-list-item 
        v-for="item in items"
        :key="item.item"
        link
      >
        <v-list-item-icon return if wide="true">
          <v-icon>{{ item.icon }}</v-icon>
        </v-list-item-icon>
        <v-list-item-content>
          <v-list-item-title>{{item.title}}</v-list-item-title>
        </v-list-item-content>
      </v-list-item>
    </v-list>
  </v-navigation-drawer>

  <!-- Sizes your content based upon application components -->
  <v-main>

    <!-- Provides the application the proper gutter -->
    <v-container grey lighten-5 class="pt-2 mr-0">

      <!-- If using vue-router -->
      <Nuxt />
    </v-container>
  </v-main>

  <v-footer app>
    <!-- -->
  </v-footer>
</v-app>
</template>

<script>
  export default {
    data (){
        return{
        drawer:false,
        items: [
          { title: 'Home', icon: 'mdi-home-variant' },
          { title: 'Explore', icon: 'mdi-compass-outline' },
          { title: 'Subscribe', icon: 'mdi-youtube-subscription' },
          { title: 'Library', icon: 'mdi-library' },
          { title: 'History', icon: 'mdi-history' },
        ],
        }
    }
  }
</script>
