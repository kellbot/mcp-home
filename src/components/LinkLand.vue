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
import {links} from '@/assets/links.json';
  function go(link) {
    window.location.href = link;
  }

  let items = links;
</script>
