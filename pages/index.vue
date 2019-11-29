<template>
  <div>
    <section>
      <v-row no-gutters>
        <v-col cols="12">
          <div class="cards">
            <figure
              class="story"
              v-for="(conf, index) in conferences"
              :key="conf.id"
            >
              <img v-lazy="conf.thumbnailImage" height="80vh" />
              <nuxt-link :to="conf.id">
                <div class="overlay">
                  <h3>{{ conf.title }}</h3>
                  <p>{{ conf.excerpt }}</p>
                 <p>n'° {{ index }}</p>
                  <v-btn
                    class="mt-2"
                    color="purple darken-2"
                    dark
                    large
                    :to="conf.id"
                  >
                    Voir l'article
                  </v-btn>
                </div>
              </nuxt-link>
            </figure>
          </div>
        </v-col>
      </v-row>
    </section>
    <section>
      <v-layout column wrap class="my-12" align-center>
        <v-flex xs12 sm4 class="my-4">
          <div class="text-center">
            <h2 class="headline">Mode Demo</h2>
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
                    <v-icon x-large class="purple--text text--darken-2"
                      >mdi-camera</v-icon
                    >
                  </v-card-text>
                  <v-card-title primary-title class="layout justify-center">
                    <div class="headline text-center">QUALITE D'IMAGE</div>
                  </v-card-title>
                  <v-card-text>
                    Cras facilisis mi vitae nunc lobortis pharetra. Nulla
                    volutpat tincidunt ornare. Pellentesque habitant morbi
                    tristique senectus et netus et malesuada fames ac turpis
                    egestas. Nullam in aliquet odio. Aliquam eu est vitae tellus
                    bibendum tincidunt. Suspendisse potenti.
                  </v-card-text>
                </v-card>
              </v-flex>
              <v-flex xs12 md4>
                <v-card flat class="transparent">
                  <v-card-text class="text-center">
                    <v-icon x-large class="purple--text text--darken-2"
                      >mdi-flash</v-icon
                    >
                  </v-card-text>
                  <v-card-title primary-title class="layout justify-center">
                    <div class="headline">UN RESEAU MOBILISABLE</div>
                  </v-card-title>
                  <v-card-text>
                    Cras facilisis mi vitae nunc lobortis pharetra. Nulla
                    volutpat tincidunt ornare. Pellentesque habitant morbi
                    tristique senectus et netus et malesuada fames ac turpis
                    egestas. Nullam in aliquet odio. Aliquam eu est vitae tellus
                    bibendum tincidunt. Suspendisse potenti.
                  </v-card-text>
                </v-card>
              </v-flex>
              <v-flex xs12 md4>
                <v-card flat class="transparent">
                  <v-card-text class="text-center">
                    <v-icon x-large class="purple--text text--darken-2"
                      >mdi-video</v-icon
                    >
                  </v-card-text>
                  <v-card-title primary-title class="layout justify-center">
                    <div class="headline text-center">Reflexion</div>
                  </v-card-title>
                  <v-card-text>
                    Cras facilisis mi vitae nunc lobortis pharetra. Nulla
                    volutpat tincidunt ornare. Pellentesque habitant morbi
                    tristique senectus et netus et malesuada fames ac turpis
                    egestas. Nullam in aliquet odio. Aliquam eu est vitae tellus
                    bibendum tincidunt. Suspendisse potenti.
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
          <div class="headline white--text mb-4 text-center">
            Bla bla bla?
          </div>
          <em>Légende pour photo</em>
          <v-btn
            class="mt-12"
            color="purple lighten-2"
            dark
            large
            href="/"
          >
            Demo
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
                Cras facilisis mi vitae nunc lobortis pharetra. Nulla volutpat
                tincidunt ornare. Pellentesque habitant morbi tristique senectus
                et netus et malesuada fames ac turpis egestas. Nullam in aliquet
                odio. Aliquam eu est vitae tellus bibendum tincidunt.
                Suspendisse potenti.
              </v-card-text>
            </v-card>
          </v-flex>
          <v-flex xs12 sm4 offset-sm1>
            <v-card flat class="transparent">
              <v-card-title primary-title class="layout justify-center">
                <div class="headline">Contact</div>
              </v-card-title>
              <v-card-text>
                Cras facilisis mi vitae nunc lobortis pharetra. Nulla volutpat
                tincidunt ornare.
              </v-card-text>
              <v-list class="transparent">
                <v-list-item>
                  <v-list-item-action>
                    <v-icon class="purple--text text--darken-2"
                      >mdi-phone</v-icon
                    >
                  </v-list-item-action>
                  <v-list-item-content>
                    <v-list-item-title>01-81-67-5309</v-list-item-title>
                  </v-list-item-content>
                </v-list-item>
                <v-list-item>
                  <v-list-item-action>
                    <v-icon class="purple--text text--darken-2"
                      >mdi-map-marker</v-icon
                    >
                  </v-list-item-action>
                  <v-list-item-content>
                    <v-list-item-title>Paris XIX, FR</v-list-item-title>
                  </v-list-item-content>
                </v-list-item>
                <v-list-item>
                  <v-list-item-action>
                    <v-icon class="purple--text text--darken-2"
                      >mdi-email</v-icon
                    >
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
    <v-footer class="py-4 deep-purple darken-2" dark height="auto">
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
          href: "#!",
          icon: "mdi-twitter"
        },
        {
          href: "#!",
          icon: "mdi-instagram"
        },
        {
          href: "#!",
          icon: "mdi-facebook"
        },
        {
          href: "#!",
          icon: "mdi-pinterest"
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
};
</script>
<style scope lang="scss">
.cards {
  @media screen and (max-width: 768px) {
    display: none;
  }
  grid-column: 1/-1;
  background-color: #eee;
  display: flex;
  white-space: nowrap;
  overflow-y: hidden;
  &::-webkit-scrollbar {
    display: none;
  }
}
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
@media screen and (max-width: 600px) {
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
  figure {
    display: inline;
  }
}

figure {
  transition: all 0.2s ease;

  position: relative;
  width: 100%;
  img {
    object-fit: cover;
  }
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
  background: rgba(255, 255, 255, 0.9); /* Black see-through */
  //color: #f1f1f1;
  width: 100%;
  height: 30%;
  transition: 0.5s ease;
  opacity: 0;
  color: black;
  font-size: 20px;
  padding: 20px;
  text-align: center;
}
</style>
