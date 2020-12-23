<template>
  <v-footer
    dark
    padless
  >
    <v-card
      class="flex"
      flat
      tile
    >
      <v-card-title class="dark">

        <v-spacer></v-spacer>

        <v-btn
          v-for="icon in icons"
          :key="icon"
          class="mx-4"
          dark
          icon
        >
          <!-- v-bindでaタグの属性値を動的に表現する -->
          <a v-bind="icon">
          <v-icon size="24px">
            {{ icon.img }}
          </v-icon>
          </a>
        </v-btn>
      </v-card-title>

      <v-card-text class="py-2 white--text text-center">
        <strong>© 2020 sometimes study</strong>
      </v-card-text>
    </v-card>
  </v-footer>
</template>
<script>
  export default {
    data: () => ({
      icons: [
        {img: 'mdi-twitter', href: 'https://twitter.com/denham95173179'},
        {img: 'mdi-github', href: 'https://hackteck.hatenablog.com/'},
        {img:'mdi-github', href: 'https://github.com/yud0uhu'},
        {img:'mdi-instagram', href: 'https://www.instagram.com/neruneruneruneu/'},
      ],
    }),
  }
</script>
