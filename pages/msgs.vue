<template>
  <v-layout>
    <v-flex xs12>
      <v-card>
        <v-container grid-list-sm fluid>
          <v-layout wrap>
            <v-flex
              v-for="n in 12"
              :key="n"
              xs6
              d-flex
              child-flex
            >
              <v-card flat tile class="d-flex">
                <v-layout>
                  <v-flex xs4>
                    <v-img
                      :src="`https://picsum.photos/500/300?image=${n * 5 + 10}`"
                      :lazy-src="`https://picsum.photos/10/6?image=${n * 5 + 10}`"
                      aspect-ratio="1"
                      class="grey lighten-2"
                      style="border-radius: 50%"
                    >
                      <template v-slot:placeholder>
                        <v-layout
                          fill-height
                          align-center
                          justify-center
                          ma-0
                        >
                          <v-progress-circular indeterminate color="grey lighten-5"></v-progress-circular>
                        </v-layout>
                      </template>
                    </v-img>
                  </v-flex>
                  <v-flex xs8 pa-4>
                    <span class="message">
                      An arrow is a graphical symbol, such as ← or →, or a pictogram, used to point or indicate direction. In its simplest form an arrow is a triangle, chevron, or concave kite, usually affixed to a line segment or rectangle, and in more complex forms a representation of an actual arrow
                    </span>
                  </v-flex>
                </v-layout>
              </v-card>
            </v-flex>
          </v-layout>
        </v-container>
      </v-card>
    </v-flex>
  </v-layout>
</template>