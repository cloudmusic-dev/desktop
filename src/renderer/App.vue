<template>
    <div id="app">
        <v-app>
            <v-navigation-drawer
                    clipped
                    permanent
            >

                <PlaylistContainer/>

            </v-navigation-drawer>

            <v-content>
                <v-container
                        class="fill-height"
                        fluid>
                    <router-view></router-view>
                </v-container>
            </v-content>
        </v-app>
    </div>
</template>

<script>
  import {Color, Titlebar} from 'custom-electron-titlebar'
  import PlaylistContainer from './PlaylistContainer'

  // eslint-disable-next-line no-new
  new Titlebar({
    backgroundColor: Color.fromHex('#800')
  })
  export default {
    name: 'cloudmusic',
    components: {PlaylistContainer},
    props: {},
    data: () => ({

    }),
    created () {
      this.$vuetify.theme.dark = true
    }
  }
</script>

<style>
    @import url('https://fonts.googleapis.com/css?family=Source+Sans+Pro');

    body {
        font-family: 'Source Sans Pro', sans-serif;
    }

    div#app {
        overflow-y: hidden;
    }
</style>
