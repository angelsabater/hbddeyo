<template>
  <v-layout>
    <v-flex xs12>
      <v-card>
        <v-container grid-list-sm fluid>
          <v-layout wrap>
            <v-flex
              v-for="n in 30"
              :key="n"
              xs2
              d-flex
              child-flex
            >
              <v-card flat tile class="d-flex">
                <v-layout>
                  <v-flex>
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
                </v-layout>
              </v-card>
            </v-flex>
          </v-layout>
        </v-container>
      </v-card>
    </v-flex>
  </v-layout>
</template>