<template>
  <v-col :key="id">
        <v-card class="mx-auto" max-width="400" nuxt>
        <v-img class="white--text"
                height="auto"
                :src="thumbnailImage">
                <v-card-title class="align-end fill-height">{{title}}</v-card-title>
                </v-img>
                <v-card-text>
                  <span>Speaker: {{speaker}}</span><br>
                  <span class="text-primary">
                    <span>At 2PM</span><br>
                    <span>{{excerpt}}</span><br>

                  </span>
                </v-card-text>
                <v-card-actions>
                  <v-btn text color="primary" nuxt :to="id">
                    Explore
                  </v-btn>
                  <v-btn nuxt text color="red">
                    Contact Us
                  </v-btn>
                </v-card-actions>
      </v-card>
  </v-col>
</template>
<script>
export default {
  props: {
    title: {
      type: String,
      required: true
    },
    excerpt: {
      type: String,
      required: true
    },
    thumbnailImage: {
      type: String,
      required: true
    },
    speaker: {
      type: String,
      required: false
    },
    time: {
      type: Date,
      required: false
    },
    id: {
      type: String,
      required: true
    }
  },
  data () {
    return {

    }
  }
}
</script>
<style lang="scss">
img {
  object-fit: cover;
}
</style>
