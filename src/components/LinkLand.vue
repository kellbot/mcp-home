<template>
  <v-card     class="mx-auto pa-2"
    max-width="400">
      <v-list>
        <v-list-subheader>SERVICES</v-list-subheader>
      <v-list-item
        v-for="item, i in items"
        :key="i"
        :title="item.title"
        :subtitle="item.subtitle"
        :value="item.link"
        color="primary"
        @click="go(item.link)"
      ><template v-slot:prepend>
          <v-icon :icon="item.icon"></v-icon>
        </template>
    </v-list-item>
    </v-list>
  </v-card>
</template>

<script setup>
  function go(link) {
    window.location.href = link;
  }

  let items = [
  {
      title: "Logitech Media Server",
      subtitle: "Music",
      icon: 'mdi-music',
      link: 'http://mcp:9000/'
    },
    {
      title: "Sonarr",
      subtitle: "TV Shows",
      icon: 'mdi-television',
      link: 'http://mcp:38989/'
    },
    {
      title: "Radarr",
      subtitle: "Movies",
      icon: 'mdi-movie',  
          link: 'http://mcp:7878/'
    },
    {
      title: "QBittorrent",
      subtitle: "Torrent Downloads",
      icon: "mdi-download",
      link: 'http://mcp:8080/'
    },
    {
      title: "Overseerr",
      subtitle: "Requests",
      icon: 'mdi-plus',
      link: 'http://mcp:5055/'
    }
  ]
</script>
