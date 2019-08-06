<template>
  <v-layout 
    class="svgBackground">
    <v-flex >
          <v-btn to="/james" style="position: absolute; bottom: 40px; right: 200px"> → back </v-btn>
    </v-flex>

  
    <v-btn
      text small
      @click.stop="addIndex(0)"
      style="position: absolute; bottom: 170px; right: 1170px;"    
    >
      ESTO
    </v-btn>

    <v-btn
      text small
      @click.stop="addIndex(1)"
      style="position: absolute; bottom: 150px; right: 1170px;"    
    >
      MATT
    </v-btn>

    <v-btn
      text small
      @click.stop="addIndex(2)"
      style="position: absolute; bottom: 130px; right: 1170px;"    
    >
      ENRICO
    </v-btn>

    <v-btn
      text small
      @click.stop="addIndex(3)"
      style="position: absolute; bottom: 110px; right: 1170px;"
    >
      DREI
    </v-btn>

    <v-btn
      text small
      @click.stop="addIndex(4)"
      style="position: absolute; bottom: 90px; right: 1170px;"    
    >
      GER
    </v-btn>

    <v-btn
      text small
      @click.stop="addIndex(5)"
      style="position: absolute; bottom: 70px; right: 1170px;"    
    >
      DEO
    </v-btn>

    <v-btn
      text small
      @click.stop="addIndex(6)"
      style="position: absolute; bottom: 50px; right: 1170px;"    
    >
      IVAN
    </v-btn>

    <v-btn
      text small
      @click.stop="addIndex(7)"
      style="position: absolute; bottom: 30px; right: 1170px;"    
    >
      GEL
    </v-btn>

    <v-dialog
      v-model="dialog"
      max-width="400"
    >
      <v-card>
        <v-card-text>
          {{messages[index].message}}
        </v-card-text>

        <v-card-actions>
          <v-spacer></v-spacer>
          <v-btn
            color="green darken-1"
            text
            @click="dialog = false"
          >
            BACK
          </v-btn>
        </v-card-actions>
      </v-card>
    </v-dialog>

</v-layout>
</template>

<script>
  export default {
    data () {
      return {
        dialog: false,
        index: 0,
        messages: [
          {message: "Happy Birthday Tura! Wish you all the best. Goodluck sa career pero tangina dapat may swimming pa din dapat tayo tsaka christmas party ahahahaha. Yun lang. Advance salamat sa libre nyo hehe 😄"},
          {message: "Yo, boi! Happiest birthdayyyy! Thank you pre naging magkagrupo tayo sa thesis. Sobrang thank you kasi ikaw yung tumayong leadersa thesis natin, siguro kung hindi ka naging grade conscious baka di rin agad tayo nakapasa sa defense. May tulong din talaga saming mga groupmates mo yung pagiging grade conscious mo eh HAHAHAHAHAHA. Thank you rin pre sa friendship gago kasi akala ko kasi talaga nung weirdo ka tas di kita magiging tropa pero di pala HAHAHAHAHAHA ayun lang thank you ulit ❤️"},
          {message: "Happy Birthday Tura!!!!! Wala na akong balita sayo gago ka. Musta na sa pinaka masipag kong tropa. Syempre magpapakain ka (spaghetti) hindi ikaw kakainin. I know one day magiging successful ka at magkakaroon ng sariling pet shop 😂😂😂 Goodluck on your journey bro, Always talk to God."},
          {message: "Happy bday tatay tura? Tanda mopaba yung pakain mong d natuloy?  Mga yaya mong may site visit ka? Chance mo na! Bawi na! Tenenenene"},
          {message: "happy birthday tura, kelan susunod na pakalamay mo? HAHAHAHA goodluck sa future. HAPPY BIRTHDAY 😗"},
          {message: "TURA HAPPY BIRTHDAY! MY WISH FOR U IS TO BECOME WHAT U WISH TO BECOME SOMEDAY AND I PRAY AND I HOPE TO SEE A BETTER DAY HAHAHAHHA"},
          {message: "Happy Birthday Ratu, enge etneb par jk. Ingats sa kakabyahe par saka wag muna mag aanak ipon muna pang gatas hahaha. More Birthdays to come. Set na yan."},
          {message: "Tura! Hindi ako vocal pero proud ako sa lahat ng mga na-achieve nating SVG ❤️ Nakikita ko naman kay Tita kung gaano sya ka-proud sayo. Swerte ng girlfriend mo sayo!! Ingatan nyo isa’t isa. Keep aiming higher, try lang tayo ng try. & reminder lang, don’t waste what u have right now stressing over the future! Cliche pero totoo. Happy Birthday Tura!!!!"},
        ]
      }
    },
    methods: {
      addIndex(index){
        this.index = index;
        this.dialog = true;
      }
    }
  }
</script>