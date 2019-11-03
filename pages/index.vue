<template>
<div>
      <section>
      <v-row no-gutters>
        <v-col cols="12">
          <div class="img-scroll">
            <nuxt-link v-for="(conf,index) in conferences" :key="conf.id" :to="conf.id">
            <figure  >
              <img v-lazy="conf.thumbnailImage" height="80vh" />
              <div class="overlay">
                <h3>{{conf.title}}</h3>
                <p>{{conf.excerpt}}</p>
                n'° {{index}}
                </div>
            </figure>
            </nuxt-link>
            <!-- <figure v-for="conf in conferences" :key="conf.id" >
              <ConfPreview
      :id='conf.id'
      :title="conf.title"
      :speaker="conf.speaker"
      :excerpt="conf.excerpt"
      :thumbnailImage="conf.thumbnailImage"
      />
            </figure> -->

          </div>
        </v-col>
      </v-row>
    </section>
    <section>
        <v-layout
          column
          wrap
          class="my-12"
          align-center
        >
          <v-flex xs12 sm4 class="my-4">
            <div class="text-center">
              <h2 class="headline">Lorem Ipsem </h2>
              <span class="subheading">
                Cras facilisis mi vitae nunc
              </span>
            </div>
          </v-flex>
          <v-flex xs12>
            <v-container grid-list-xl>
              <v-layout row wrap align-center>
                <v-flex xs12 md4>
                  <v-card flat class="transparent">
                    <v-card-text class="text-center">
                      <v-icon x-large class="purple--text text--darken-2">mdi-camera</v-icon>
                    </v-card-text>
                    <v-card-title primary-title class="layout justify-center">
                      <div class="headline text-center">QUALITE D'IMAGE</div>
                    </v-card-title>
                    <v-card-text>
                      Cras facilisis mi vitae nunc lobortis pharetra. Nulla volutpat tincidunt ornare.
                      Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas.
                      Nullam in aliquet odio. Aliquam eu est vitae tellus bibendum tincidunt. Suspendisse potenti.
                    </v-card-text>
                  </v-card>
                </v-flex>
                <v-flex xs12 md4>
                  <v-card flat class="transparent">
                    <v-card-text class="text-center">
                      <v-icon x-large class="purple--text text--darken-2">mdi-flash</v-icon>
                    </v-card-text>
                    <v-card-title primary-title class="layout justify-center">
                      <div class="headline">UN RESEAU MOBILISABLE</div>
                    </v-card-title>
                    <v-card-text>
                      Cras facilisis mi vitae nunc lobortis pharetra. Nulla volutpat tincidunt ornare.
                      Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas.
                      Nullam in aliquet odio. Aliquam eu est vitae tellus bibendum tincidunt. Suspendisse potenti.
                    </v-card-text>
                  </v-card>
                </v-flex>
                <v-flex xs12 md4>
                  <v-card flat class="transparent">
                    <v-card-text class="text-center">
                      <v-icon x-large class="purple--text text--darken-2">mdi-video</v-icon>
                    </v-card-text>
                    <v-card-title primary-title class="layout justify-center">
                      <div class="headline text-center">Reflexion</div>
                    </v-card-title>
                    <v-card-text>
                      Cras facilisis mi vitae nunc lobortis pharetra. Nulla volutpat tincidunt ornare.
                      Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas.
                      Nullam in aliquet odio. Aliquam eu est vitae tellus bibendum tincidunt. Suspendisse potenti.
                    </v-card-text>
                  </v-card>
                </v-flex>
              </v-layout>
            </v-container>
          </v-flex>
        </v-layout>
      </section>

      <section>
        <v-parallax :src="require('../assets/section.jpg')" height="380">
          <v-layout column align-center justify-center>
            <div class="headline white--text mb-4 text-center">Web development has never been easier</div>
            <em>Kick-start your application today</em>
            <v-btn
              class="mt-12"
              color="purple lighten-2"
              dark
              large
              href="/pre-made-themes"
            >
              Get Started
            </v-btn>
          </v-layout>
        </v-parallax>
      </section>

<section>
        <v-container grid-list-xl>
          <v-layout row wrap justify-center class="my-12">
            <v-flex xs12 sm4>
              <v-card flat class="transparent">
                <v-card-title primary-title class="layout justify-center">
                  <div class="headline">info</div>
                </v-card-title>
                <v-card-text>
                  Cras facilisis mi vitae nunc lobortis pharetra. Nulla volutpat tincidunt ornare.
                  Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas.
                  Nullam in aliquet odio. Aliquam eu est vitae tellus bibendum tincidunt. Suspendisse potenti.
                </v-card-text>
              </v-card>
            </v-flex>
            <v-flex xs12 sm4 offset-sm1>
              <v-card flat class="transparent">
                <v-card-title primary-title class="layout justify-center">
                  <div class="headline">Contact</div>
                </v-card-title>
                <v-card-text>
                  Cras facilisis mi vitae nunc lobortis pharetra. Nulla volutpat tincidunt ornare.
                </v-card-text>
                <v-list class="transparent">
                  <v-list-item>
                    <v-list-item-action>
                      <v-icon class="purple--text text--darken-2">mdi-phone</v-icon>
                    </v-list-item-action>
                    <v-list-item-content>
                      <v-list-item-title>01-81-67-5309</v-list-item-title>
                    </v-list-item-content>
                  </v-list-item>
                  <v-list-item>
                    <v-list-item-action>
                      <v-icon class="purple--text text--darken-2">mdi-map-marker</v-icon>
                    </v-list-item-action>
                    <v-list-item-content>
                      <v-list-item-title>Paris XIX, FR</v-list-item-title>
                    </v-list-item-content>
                  </v-list-item>
                  <v-list-item>
                    <v-list-item-action>
                      <v-icon class="purple--text text--darken-2">mdi-email</v-icon>
                    </v-list-item-action>
                    <v-list-item-content>
                      <v-list-item-title>you@teambouesso.com</v-list-item-title>
                    </v-list-item-content>
                  </v-list-item>
                </v-list>
              </v-card>
            </v-flex>
          </v-layout>
        </v-container>
      </section>
      <v-footer
    class="py-4 deep-purple darken-2"
    dark
    height="auto"
  >
    <v-container mx-auto>
      <v-layout wrap>
        <v-flex xs9>
          <v-btn
            v-for="(item, i) in items"
            :key="i"
            :href="item.href"
            class="ml-0 mr-3"
            color="white"
            text
            icon
            target="_blank"
          >
            <v-icon v-text="item.icon" />
          </v-btn>
        </v-flex>
        <v-spacer />
        <v-btn
          class="mr-0"
          icon
          text
          title="Go to top"
          @click="$vuetify.goTo(0)"
        >
          <v-icon>mdi-chevron-up</v-icon>
        </v-btn>
      </v-layout>
    </v-container>
  </v-footer>
</div>
  <!--   <v-container fluid>
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



  </v-container>-->



</template>

<script>
import ConfPreview from "@/components/Conference/ConfPreview";
export default {
  components: {
    ConfPreview
  },
  data() {
    return {
      img: [
        "https://placeimg.com/450/450/arch",
        "https://placeimg.com/450/450/nature",
        "https://placeimg.com/450/450/people",
        "https://placeimg.com/450/450/arch",
        "https://placeimg.com/450/450/nature",
        "https://placeimg.com/450/450/people",
        "https://placeimg.com/450/450/tech"
      ],
      items: [
        {
          href: '#!',
          icon: 'mdi-twitter'
        },
        {
          href: '#!',
          icon: 'mdi-instagram'
        },
        {
          href: '#!',
          icon: 'mdi-facebook'
        },
        {
          href: '#!',
          icon: 'mdi-pinterest'
        }
      ]
    };
  },
  asyncData(context) {
    return context.app.$storyapi
      .get("cdn/stories", {
        version: process.env.NODE_ENV == "production" ? "published" : "draft",
        starts_with: "conference/"
      })
      .then(res => {
        console.log("hey hey hey", res.data.stories);
        return {
          conferences: res.data.stories.map(c => {
            return {
              id: c.slug,
              title: c.content.title,
              thumbnailImage: c.content.thumbnail,
              speaker: c.content.speaker,
              excerpt: c.content.summary
            };
          })
        };
      });
  }
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
};
</script>
<style scope>
* {
  box-sizing: border-box;
}
a,
li {
  text-decoration: none;
}
img {
  height: 100vh;
  /* width: 50vw; */
  padding: 0;
  display: block;
}
@media  screen and (max-width: 600px) {
  img {
    height: 65vh;
    width: 100vw;
  }
  .img-scroll {
  display: inline-block;


}
.overlay:last-child {
  width: 115%;
}
figure{
  display: inline;
}
}

figure {
  transition: all 0.2s ease;

  position: relative;
  width: 100%;
  /* max-width: 300px; */
}
figure:hover .overlay {
  opacity: 1;

}

.img-scroll {
  display: flex;
  overflow-x: auto;


}

.overlay {
  position: absolute;
  bottom: 0;
  display: block;
  background: rgb(0, 0, 0);
  background: rgba(0, 0, 0, 0.5); /* Black see-through */
  color: #f1f1f1;
  width: 100%;
  height: 30%;
  transition: 0.5s ease;
  opacity: 0;
  color: white;
  font-size: 20px;
  padding: 20px;
  text-align: center;
}
</style>
