<template>
  <v-container fluid>
    <v-layout row wrap>
    <v-flex layout align-center justify-center column fill-height v-for="conf in conferences" :key="conf.id" xs12 md6 sm6 lg3 xl3>
      <template >
      <ConfPreview
      :id='conf.id'
      :title="conf.title"
      :speaker="conf.speaker"
      :excerpt="conf.excerpt"
      :thumbnailImage="conf.thumbnailImage"
      />
    </template>
    </v-flex>
    </v-layout>
  </v-container>
</template>

<script>
import ConfPreview from "@/components/Conference/ConfPreview";
export default {
  components: {
    ConfPreview
  },
  asyncData(context) {
    return context.app.$storyapi.get('cdn/stories', {
      version: process.env.NODE_ENV == 'production'? 'published' : 'draft',
      starts_with: 'conference/'
    }).then(res => {
      console.log('hey hey hey',res.data.stories)
      return {
        conferences:res.data.stories.map(c => {
        return {
                id: c.slug,
                title: c.content.title,
                thumbnailImage: c.content.thumbnail,
                speaker:c.content.speaker,
                excerpt: c.content.summary
        }
      })}
    })
  },
/*   data() {
    return {
      conferences: [
        {
          title: "How to become a Pro",
          previewtext: "Here is what I learn for my own experience",
          thumbnailUrl: "http://blog.fieldoo.com/wp-content/uploads/2014/09/how-to-become-a-professional-football_soccer-player.jpg",
          speaker: "Bob Denver",
          id: 'how-to-be-pro'
        },
        {
          title: "What I do not learn from school",
          previewtext: "Here is what I learn for my own experience",
          thumbnailUrl: "https://www.brainyquote.com/photos_tr/en/w/willsmith/451157/willsmith1-2x.jpg",
          speaker: "Tsubasa Ozora",
          id: 'not-learn-from-school'
        },
        {
          title: "To my younger self",
          previewtext: "Please follow my advices",
          thumbnailUrl: "https://www.brainyquote.com/photos_tr/en/w/willsmith/451157/willsmith1-2x.jpg",
          speaker: "Mark Landers",
          id: 'to-my-younger-self'
        }
        {
          title: "How to become a Pro part 2",
          previewtext: "Here is what I learn for my own experience",
          thumbnailUrl: "http://blog.fieldoo.com/wp-content/uploads/2014/09/how-to-become-a-professional-football_soccer-player.jpg",
          speaker: "Bob Denver",
          id: 'how-to-be-pro'
        }
      ]
      }
    } */

  }

</script>
<style scope>
a,li{
  text-decoration: none;
}
</style>
