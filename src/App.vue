  
<template>
  <v-app id="inspire">
    <v-navigation-drawer 
      v-model="drawer"
      app
    >
      <v-list-item>
        <v-list-item-content>
          <v-list-item-title class="title">
            Application
          </v-list-item-title>
          <v-list-item-subtitle>
            subtext
          </v-list-item-subtitle>
        </v-list-item-content>
      </v-list-item>

      <v-divider></v-divider>

      <v-list
        dense
        nav
      >
        <v-list-item
          v-for="item in items"
          :key="item.title"
          link
        >
          <v-list-item-icon>
            <v-icon>{{ item.icon }}</v-icon>
          </v-list-item-icon>

          <v-list-item-content>
            <v-list-item-title>{{ item.title }}</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>

    <v-app-bar 
      color="blue darken-1"
    
    app>
      <v-app-bar-nav-icon @click="drawer = !drawer"></v-app-bar-nav-icon>
      <v-img
        lazy-src="https://amcui.ig.he-arc.ch/images/auto-multiple-choice.78dc45ea.svg"
        max-height="24"
        max-width="24"
        src="https://amcui.ig.he-arc.ch/images/auto-multiple-choice.78dc45ea.svg"
      ></v-img>
      <v-toolbar-title font="white">Grade Manager (AMC-UI)</v-toolbar-title>
      <v-spacer></v-spacer>
      <v-btn icon>
        <v-icon>mdi-book-open-page-variant-outline</v-icon>
      </v-btn>
    </v-app-bar>

    <v-main>
      <v-card
        class="mx-auto my-12"
        max-width="374"
      >
        <v-input >
            <v-text-field
            label="Username"
            class="my-4"
          ></v-text-field>
        </v-input>
        <v-input>
          <v-text-field
          label="Password"
          ></v-text-field>
        </v-input>
         <v-card-actions>
            <v-btn
              color="deep-purple lighten-2"
              text
              @click="reserve"
            >
              Login
            </v-btn>
               <v-btn
              color="deep-purple lighten-2"
              text
              @click="reserve"
            >
              Create
            </v-btn>
        </v-card-actions>
      </v-card>
  
    </v-main>
  </v-app>
</template>

<script>
  export default {
    data: () => ({ 
      drawer: null,
      items: [
          { title: 'Dashboard', icon: 'mdi-view-dashboard' },
          { title: 'Photos', icon: 'mdi-image' },
          { title: 'A propos', icon: 'mdi-help-box' },
        ],
      }),
  }
</script>