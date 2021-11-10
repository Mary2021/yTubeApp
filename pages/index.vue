<template> 
  <v-row
    class="fill-height pa-2"
    align="center"
    justify="center"
    width="270px"
  >
    <template v-for="(item, i) in items">
      <v-col
        :key="i"
        cols="12"
        md="3"
      >
        <v-hover v-slot="{ hover }">
          <v-card--flat
            width="270px"
            :elevation="hover ? 12 : 2"
            :class="{ 'on-hover': hover }"
          >
            <v-img
              :src="item.img"
              height="150px"
            ></v-img> 
            <v-container>
              <v-row>
              <v-col         
                cols="2"
                class="pl-0"
              >
                <v-avatar
                  height="36"
                  width="36" 
                >
                  <img
                    :src="item.avatar"
                    alt="Avatar"
                  > 
                </v-avatar>
              </v-col>
              <v-col>
              <v-card-text class="pa-0 black--text font-weight-bold text-left">
                {{ item.title }}
              </v-card-text>
              <v-card-text class="pa-0 grey--text text-left">
                {{ item.text }}
              </v-card-text>
              <v-card-text class="pa-0 grey--text text-left">
                {{ item.subtext }}
              </v-card-text>
              </v-col>
              </v-row>
            </v-container>
          </v-card--flat>
        </v-hover>
      </v-col>
    </template>
  </v-row>

</template>

<script>
  export default {
    data: () => ({
      items: [
        {
          img: "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRgXyuMaBqZfRKACzkjpettHKr_wuvgHfd6wg&usqp=CAU",
          avatar: "https://yt3.ggpht.com/ytc/AKedOLSDxCdSSEYm21Gr8W40aB3EyNVGzwyEUe8uS8xnPA=s88-c-k-c0x00ffffff-no-rj",
          title: "#11 Update Quantity of Shopping Cart with MVC",
          text: "Learning Programming",
          subtext: "3,139 views Jan 2018",
        },
        {
          img: "https://i.ytimg.com/vi/36YnV9STBqc/hq720.jpg?sqp=-oaymwEcCNAFEJQDSFXyq4qpAw4IARUAAIhCGAFwAcABBg==&rs=AOn4CLAT4S3oWIcYxrETqc5vVfey9Yj24A",
          avatar: "https://yt3.ggpht.com/ytc/AKedOLRolK5uaMIsmYQV2cHzxxC8qSCH5aQ18O3_PMJHwQ=s88-c-k-c0x00ffffff-no-rj",
          title: "The Good Life Radio",
          text: "The Good Life Radio x Sensual Musique",
          subtext: "9,599 watching now",
        },
                {
          img: "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSjz5_LN8AX5K8Vq0b8x5tdoByWPZ9bASY7Fg&usqp=CAU",
          avatar: "https://yt3.ggpht.com/ytc/AKedOLTqtZ7NA_GLq8AStdNh-1JekW9KNKIsvSCTOWQ7UA=s176-c-k-c0x00ffffff-no-rj-mo",
          title: "Touring a $100,000,000 Brand New MEGAYACHT",
          text: "Enes Yilmazer",
          subtext: "1.4M subscribers",
        },
                {
          img: "https://images.unsplash.com/photo-1429514513361-8fa32282fd5f?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=3264&q=80",
          avatar: "https://cdn.vuetifyjs.com/images/john.jpg",
          title: "Newly released songs. Updated daily.",
          text: "New Release Friday",
          subtext: "517,368 views",
        },
                        {
          img: "https://i.ytimg.com/vi/zPNi78sVbio/hqdefault_live.jpg?sqp=-oaymwEcCNACELwBSFXyq4qpAw4IARUAAIhCGAFwAcABBg==&rs=AOn4CLCUCNfYoQW9cZrpoggqv-ZPvcbgDQ",
          avatar: "https://cdn.vuetifyjs.com/images/john.jpg",
          title: "Chill Music for Focus and Creativity",
          text: "Music Lab",
          subtext: "458K subscribers",
        },
                        {
          img: "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTEVMcZzUXlFqkDbNE9ykXzK3esvOprJNzpoQ&usqp=CAU",
          avatar: "https://yt3.ggpht.com/ytc/AKedOLTK0y25C0RJiEngT1ae9mrZLXIortPD-DKQxOlRkw=s88-c-k-c0x00ffffff-no-rj",
          title: "Windows 11 is bigger than we thought",
          text: "Linus Tech Tips",
          subtext: "14.1M subscribers",
        },
                        {
          img: "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRSR5JUpYYHilYxdAF5trND3rVLk8K4FJOZow&usqp=CAU",
          avatar: "https://yt3.ggpht.com/5oUY3tashyxfqsjO5SGhjT4dus8FkN9CsAHwXWISFrdPYii1FudD4ICtLfuCw6-THJsJbgoY=s88-c-k-c0x00ffffff-no-rj",
          title: "Buying Anything My Dog Touches",
          text: "PewDiePie",
          subtext: "110M subscribers",
        },
                        {
          img: "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQbiOiVXCFAuM8QTrTZjtHYAj7CWmuSYkBEXw&usqp=CAU",
          avatar: "https://yt3.ggpht.com/ytc/AKedOLSJN0Dyxz8t9bx4n5UgmJCrMaAcprFai4z9_aj3nA=s88-c-k-c0x00ffffff-no-rj",
          title: "I Cleaned The World’s Dirtiest Beach",
          text: "MrBeast",
          subtext: "73.3M subscribers",
        },
                        {
          img: "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcROLElisW2fzZY9EbICfuSYFOg7m70LCxoGrw&usqp=CAU",
          avatar: "https://yt3.ggpht.com/ytc/AKedOLR6sZuGVydaGaPQ6HOSrpuhUurjXgs2_SNKv2qu9Q=s88-c-k-c0x00ffffff-no-rj",
          title: "New 2022 Toyota bZ4X - Pure-Electric Compact SUV",
          text: "Power Torque",
          subtext: "184,203 views",
        },
                        {
          img: "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRWcBKr9l8V9cHF_iCpyQnp4k_xoO_i0O9n1Q&usqp=CAU",
          avatar: "https://yt3.ggpht.com/wKsXXrYDK98FHYqjAwsVrCxCQ2ksqpUb8UEcNt0jiQXhC_Le3LrS3S_pH8uCwkbbjLVlpNLr5w=s88-c-k-c0x00ffffff-no-rj",
          title: "Simona Halep vs. Anett Kontaveit | 2021",
          text: "WTA",
          subtext: "284K subscribers",
        },
                        {
          img: "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQ4FEInVBGYK8YW4e9rU9vRubROj1lPvBiDFg&usqp=CAU",
          avatar: "https://yt3.ggpht.com/ytc/AKedOLRxsxjCfqWp9gTfiMIeoqoCeJsln_y6aXGXUSRf=s88-c-k-c0x00ffffff-no-rj",
          title: "Egyptology - Pyramid Construction",
          text: "Naked Science",
          subtext: "1.13M subscribers",
        },
                        {
          img: "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTSloIkHE1ey15sAIjXk0QB_yVfPXe6jWmfYg&usqp=CAU",
          avatar: "https://yt3.ggpht.com/ytc/AKedOLQh9hGECGZoKZqNzL4yVdQ0qavEYkRXo8FirxHo=s88-c-k-c0x00ffffff-no-rj",
          title: "Golden Retriever Meets Puppies for the First Time",
          text: "This is Bailey",
          subtext: "366K subscribers",
        },
      ],
    }),
  }
</script>

<style>

</style>
