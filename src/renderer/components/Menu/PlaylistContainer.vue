<template>
    <v-list dense>
        <v-subheader>
            <v-icon>mdi-playlist-music</v-icon>
            PLAYLISTS
        </v-subheader>
        <v-list-item link>
            <v-list-item-action>
                <v-icon>mdi-playlist-plus</v-icon>
            </v-list-item-action>
            <v-list-item-content>
                <v-list-item-title>New Playlist</v-list-item-title>
            </v-list-item-content>
        </v-list-item>
        <v-list-item v-for="playlist in playlists" :key="playlist.id" link>
            <v-list-item-action>
                <v-icon>mdi-view-dashboard</v-icon>
            </v-list-item-action>
            <v-list-item-content>
                <v-list-item-title>{{playlist.name}}</v-list-item-title>
            </v-list-item-content>
        </v-list-item>
    </v-list>
</template>
<script>
  export default {
    name: 'PlaylistContainer',
    data: function () {
      return {
        playlists: []
      }
    }
  }
</script>
