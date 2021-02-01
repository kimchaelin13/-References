<template>
    <div id="#app">
        <v-app id="inspire">
            <v-card
            width="256"
            height="70rem"
            tile
        >
            <v-navigation-drawer permanent>
                <h1>Komenta</h1>
                <v-list>
                    <v-list-item>
                        <v-list-item-avatar>
                            <v-img src="https://cdn.vuetifyjs.com/images/john.png"></v-img>
                        </v-list-item-avatar>
                    </v-list-item>
  
                    <v-list-item link>
                        <v-list-item-content>
                            <v-list-item-title class="title">
                                John Leider
                            </v-list-item-title>
                            <v-list-item-subtitle>john@vuetifyjs.com</v-list-item-subtitle>
                        </v-list-item-content>
  
                        <v-list-item-action>
                            <v-icon>mdi-menu-down</v-icon>
                        </v-list-item-action>
                        </v-list-item>
                        </v-list>
                        <v-divider></v-divider>
                        <v-list
                            nav
                            dense
                        >
                        <v-list-item-group
                            v-model="selectedItem"
                            color="primary"
                        >
                        
                        <v-list-item
                        v-for="(item, i) in items"
                        :key="i"
                        >
                        <v-list-item-icon>
                            <v-icon v-text="item.icon"></v-icon>
                        </v-list-item-icon>
  
                        <v-list-item-content>
                            <v-list-item-title v-text="item.text"></v-list-item-title>
                        </v-list-item-content>
                    </v-list-item>
          </v-list-item-group>
        </v-list>
      </v-navigation-drawer>
    </v-card>
  </v-app>
    </div>

</template>

<script>

export default {
    // el: '#app',

    name: 'asidebar',
    data:() => ({
        selectedItem: 0,
        items: [
        { text: 'Home', icon: 'home' },
        { text: 'My Streaming List', icon: 'album' },
        { text: 'VOD', icon: 'ondemand_video' },
        { text: 'My Feed', icon: 'mdi-check-circle' },
        { text: 'My Page', icon: 'account_circle' },
        { text: '고객센터', icon: 'support_agent' },
        ],
    }),
    mounted() {
        
    },
    methods: {
        
    },
};
</script>

<style scoped>
    /* #app {
        width: 200px;
        display: inline-block;
        background-color: yellowgreen;
    } */
</style>