<template>
 
  <v-app id="inspire">
    

    <v-app-bar app  height="60">
      <v-app-bar-nav-icon @click="drawer = !drawer"></v-app-bar-nav-icon>


     
 <v-responsive max-width="300" >
      <v-autocomplete 
      clearable
      rounded
      solo
      color="blue"
      placeholder=" سرچ کنید..."
      ></v-autocomplete>
      </v-responsive>

      <v-spacer></v-spacer>

      <v-app-bar-nav-icon></v-app-bar-nav-icon>
      <v-app-bar-nav-icon></v-app-bar-nav-icon>
      <v-app-bar-nav-icon></v-app-bar-nav-icon>
      
  
      


</v-app-bar>

    <v-navigation-drawer
      v-model="drawer"
      app
      right
    ><!-- fixed
      temporary  -->

 <v-sheet
        color="grey lighten-4"
        class="pa-4"
      >
        <v-avatar
          class="mb-4"
          color="grey darken-1"
          size="64"
        ></v-avatar>

        <div> byd@talash.com</div>
      </v-sheet>

      <v-divider></v-divider>

      <v-list>
        <v-list-item
          v-for="[icon, text] in links"
          :key="icon"
          link
        >
          <v-list-item-icon>
            <v-icon>{{ icon }}</v-icon>
          </v-list-item-icon>

          <v-list-item-content>
            <v-list-item-title>{{ text }}</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list>

    </v-navigation-drawer>

    
    
    
    <v-main>
      <!--  -->
    </v-main>
  
  </v-app>
</template>

<script>
  export default {
      methods: {
      changeRTL () {
      this.$vuetify.rtl = true
      },
    },
   data: () => ({
      
      drawer: null,
      links: [
        ['mdi-inbox-arrow-down', 'Inbox'],
        ['mdi-send', 'Send'],
        ['mdi-delete', 'Trash'],
        ['mdi-alert-octagon', 'Spam'],
      ],
    }),
  }
</script>