<template>
  <v-container>
    <v-card
      justify-center
      class="mx-auto"
    >
      <v-system-bar
        color="pink darken-2"
        dark
      >
        <v-spacer />

        <v-icon>mdi-window-minimize</v-icon>

        <v-icon>mdi-window-maximize</v-icon>

        <v-icon>mdi-close</v-icon>
      </v-system-bar>

      <v-app-bar
        dark
        color="pink"
      >
        <v-app-bar-nav-icon />

        <v-toolbar-title
          justify-center
        >
          My Profile
        </v-toolbar-title>

        <v-spacer />

        <v-btn icon>
          <v-icon>mdi-magnify</v-icon>
        </v-btn>
      </v-app-bar>
      <v-row dense>
        <v-col cols="12">
          <v-card
            color="#385F73"
            dark
          >
            <v-card-title class="headline">
              Self-Introduction
            </v-card-title>

            <v-card-subtitle>Software Engineer</v-card-subtitle>

            <v-card-text>
              Skills:</br>
              Ruby,JavaScript,SQL,GitHub,Linux,AWS,Scrum</br>
              Frameworks:</br>
              Ruby on Rails,Vue.js,Nuxt.js</br>
              Other Fields:</br>
              Inferential statistics,Bayesian statistics,Accounting,Finance,Quants analysis
            </v-card-text>

            <v-card-actions>
              <v-btn text href="https://github.com/LFTKazu">
                GitHub
              </v-btn>
            </v-card-actions>
          </v-card>
        </v-col>

        <v-col
          v-for="(item, i) in items"
          :key="i"
          cols="12"
        >
          <v-card
            :color="item.color"
            dark
          >
            <div class="d-flex flex-no-wrap justify-space-between">
              <div>
                <v-card-title
                  class="headline"
                  v-text="item.title"
                />

                <v-card-subtitle v-text="item.artist" />

                <v-card-actions>
                  <v-btn
                    v-if="item.artist === ''"
                    class="ml-2 mt-3"
                    fab
                    icon
                    height="40px"
                    right
                    width="40px"
                  >
                    <v-icon>mdi-play</v-icon>
                  </v-btn>

                  <v-btn
                    v-else
                    class="ml-2 mt-5"
                    outlined
                    rounded
                    small
                    href="https://fargate.hatenablog.com/"
                  >
                    MyBlog
                  </v-btn>
                </v-card-actions>
              </div>

              <v-avatar
                class="ma-3"
                size="125"
                tile
              >
                <v-img :src="item.src" />
              </v-avatar>
            </div>
          </v-card>
        </v-col>
      </v-row>
    </v-card>
  </v-container>
  </v-card>
</template>

<script>
export default {
  data: () => ({
    items: [
      {
        color: '#1F7087',
        src: 'icon9.png',
        title: 'Experiences',
        artist: 'Smartphone E-commerce site Replace,Cosme E-commerce site Replace,Cryptocurrency exchange'
      },
      {
        color: '#952175',
        src: '',
        title: 'To Be Continue...',
        artist: ''
      }
    ]
  })
}
</script>
