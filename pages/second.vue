<template>
  <v-layout>
    <v-flex xs6 sm6>
      <v-card>
        <v-container grid-list-sm fluid>
          <v-layout wrap>
            <v-flex
              v-for="n in 4"
              :key="n"
              xs6
              d-flex
              child-flex
            >
              <v-card 
                flat 
                tile 
                :elevation = 0
              >
                <v-img
                  :src="`https://picsum.photos/500/300?image=${n * 5 + 10}`"
                  :lazy-src="`https://picsum.photos/10/6?image=${n * 5 + 10}`"
                  aspect-ratio="1"
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
              </v-card>
            </v-flex>
          </v-layout>
        </v-container>
      </v-card>
    </v-flex>
    <v-flex x6>
      <v-layout
        column
        fill-height
        align-center
        justify-center
        text-xs-center>
        <div>
          <span class="secondtext">
            Happy Birthday Deo.
          </span>
          <br>
          <v-btn class="my-2" to="/svg"> → svg </v-btn>
          <v-btn class="my-2" to="/svgmsg"> → svg msg </v-btn>
          <v-btn class="my-2" to="/friends"> → msgs </v-btn>
        </div>
      </v-layout>
    </v-flex>

  </v-layout>
</template>