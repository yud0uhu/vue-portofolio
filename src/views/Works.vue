<template>
  <v-timeline>
    <v-timeline-item
      v-for="(year, i) in years"
      :key="i"
      :color="year.color"
      small
    >
      <template v-slot:opposite>
        <span
          :class="`headline font-weight-bold ${year.color}--text`"
          v-text="year.year"
        ></span>
      </template>
      <div class="py-4">
        <h2 :class="`headline font-weight-light mb-4 ${year.color}--text`">Works</h2>
        <div>
          {{year.skill}}:{{year.datail}}
          <a v-bind="year">
          <v-img
            :src="`https://picsum.photos/500/300?image=${i * 5 + 10}`"
            :lazy-src="`https://picsum.photos/10/6?image=${i * 5 + 10}`"
            aspect-ratio="1"
            max-height="150"
            max-width="250"
            ></v-img>
            </a>
        </div>
      </div>
    </v-timeline-item>
  </v-timeline>
</template>

<script>
  export default {
    data: () => ({
      years: [
        {
          color: 'cyan',
          year: '2020-03',
          skill: 'Glide,GAS',
          datail: 'Chitose City × Curry Search',
          href: 'https://currysearchlink.glideapp.io/',
        },
        {
          color: 'green',
          year: '2020-08',
          skill: 'Glide,GAS',
          datail: 'Chitose City × TAKEOUT FOOD Search',
          href: 'https://probable-point-1725.glideapp.io/',
        },
        {
          color: 'pink',
          year: '2020-08',
          skill: 'Unity 1 Week Works',
          datail: 'Unity',
          href: 'https://unityroom.com/games/a2wvzg5b'
        },
        {
          color: 'amber',
          year: '2020-09',
          skill: 'HTML/CSS/GitHubPages',
          datail: 'portofolio',
          href: 'https://yud0uhu.github.io/unikuri/',
        },          
        {
          color: 'amber',
          year: '2020-10',
          skill: 'HTML/CSS/firebase',
          datail: 'portofolio',
          href: 'https://my-portofolio-4e7d9.web.app/',
        },  
        {
          color: 'amber',
          year: '2020-11',
          skill: 'GAS/HTML/CSS/Vue.js/jQuery/firebase',
          datail: 'Chitose City × TAKEOUT FOOD Search (WEB版)',
          href: 'https://chitose-fts.web.app/',
        },               
        {
          color: 'amber',
          year: '2020-11',
          skill: 'React.js/firebase',
          datail: 'Youtube Clone App',
          href: 'https://react-clone-eb00b.web.app/',
        },
        {
          color: 'orange',
          year: '2020-12',
          skill: 'Vue.js/Vuetify/firebase',
          datail: 'portofolio',
          href: 'https://yukimi-pino.web.app/',
        },
      ],
    }),
  }
</script>
