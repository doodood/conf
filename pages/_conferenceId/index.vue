<template>
  <div id="conf" v-editable="blok">

    <div id="conf-thumbnail" :style="{backgroundImage: 'url('+thumbnail+')'}">

    </div>
    <v-container fluid>
      return to <nuxt-link to="/">home</nuxt-link>
      <h1>{{title}}</h1>
    <p>{{content}}</p>
    </v-container>

  </div>
</template>
<script>
export default {
  asyncData(context) {
    return context.app.$storyapi.get(`cdn/stories/conference/${context.params.conferenceId}`, {
      version: process.env.NODE_ENV == "production" ? "published" : "draft"
    }).then(res => {
      return {
        blok: res.data.story.content,
          thumbnail : res.data.story.content.thumbnail,
          description : res.data.story.content.summary,
          content:res.data.story.content.content,
          speaker: res.data.story.content.speaker,
          title: res.data.story.content.title
      }
    })
  },
  mounted() {
    /* this.$storybridge.on(['published', 'change'], (event) => {
      if (!event.slugChanged) {
        // Reload the page on save events (publish, save button or autosave)
        this.$nuxt.$router.go({
          path: this.$nuxt.$router.currentRoute,
          force: true
        })
      }
    }) */
  }
}
</script>
<style >
#conf-thumbnail{
  width: 100%;
  height: 95vh;
  background-size: cover;
  background-position: center;
  object-fit: cover;
}

</style>
