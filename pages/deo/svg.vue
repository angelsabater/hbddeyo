<template>
  <v-layout 
    class="svgBackground">
    <v-flex >
          <v-btn to="/deo" style="position: absolute; bottom: 40px; right: 200px"> → back </v-btn>
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
      TURA
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
          {message: "Happy Birthday Deyo! Wish you all the best. Goodluck sa career pero tangina dapat may swimming pa din dapat tayo tsaka christmas party ahahahaha. Yun lang. Advance salamat sa libre nyo hehe 😄"},
          {message: "Yo, taba! Happiest birthdayyyy! Thank you for being the leader aka tatay ng svg kasi pag ikaw nagpaplano laging natutuloy. Dati nga diba hindi ka pa nakasama kasi nagkasakit ka pero at least natuloy HAHAHAHAHAHA. Thank you sa friendship na hindi friends ang turingan kundi family. Thank you sa pagtulong mo lagi samin kahit na busy ka rin. Thank you sa lahat ng reviewer na hiningi ko sayo kasi pumasa ako dahil sayo HAHAHAHAHA. Sana wag ka magbago, tanggap ka naman namin kahit mataba ka no joke to HAHAHAHAHAHA ayun lang thank you ulit 💕"},
          {message: "Hoy deyo!!!! hindi ka naman kagalang-galang bat pa babatiin jusko. hahahahahahahaha. Happy Birthday taba! Dalawa lang sasabihin ko, una, i want you to know that i am proud of who you are now and what you have become, keep achieving your goal, im here whenever need me. Pangalawa, namimiss ko yung murahan natin sa thesis, namimiss ko yung awayin natin kahit nangbbackstab ka at kayong mga RVG hahahahahaha. Joke lang 😂😂 enjoy your day, God bless you 😇"},
          {message: "Para kay deo na mahina mag lol, mahina sa lahat ng bagay, sa pagkain lang malakas, happy bornday, pakain ka naman noh puro samgyup ka sa iba mong tropa kami hirap kang magpakita, iintayin ko sweldo mo sept 1 matik na hahahhaha"},
          {message: "happy birthday deyo, tinigil ko pa nood ng spiderman dito ahh. tara na sa inyo pancit canton and chill dala ako 4k endgame wkwkkw tayong dalawa lang 😉 btw, goodluck sa future. HAPPY BIRTHDAY 😗"},
          {message: "Haappyyyyy birthday deyooo, sana lumaki ka ng may takot sa diyos, maging mabait, masunurin ka sa mga magulang mo, jk hahahah HAPPYY BIRTHDAY UWOOO!? sana maging masaya ka sa birthday mo , kailan na maseset sa bahay nyo hayss ang tagal naman, more birthday to comee, ps. pumapayat kana hehehe ngayon lang 😁😁😁"},
          {message: "Happy Birthday Deo Bamba, maraming salamat dahil palagi kang nanjan pag nanjan ka. Ingat palagi pre saka iwas na sa late hahaha. Wishing for more birthdays to come, libre mo na kami."},
          {message: "Happy Birthday Deyo! Ano pa ba sasabihin ko nasabi ko naman na kada birthday mo & kung kailan ko man gustong sabihin nararamdaman ko dba haha. Alam mo naman kung gano ako ka-proud sayo, sa mga achievements mo. Lagi lang andito yung SVG para sayo, para sa isa’t-isa dba? Kahit ano kaya natin basta svg. Miss ko na kayo! Alis tayo paguwi ko ha! 😊 Life tip from the girl who’s far: try to learn new things everyday! Your future self will thank you later! I’ll always be one step behind you, to support & cheer for you backstage or even beside you! 🤘🏻 I just want to remind you to not waste your present stressing over the future! & hindi lang ako nandito para sa magagandang parte ng buhay pwede mo kong kausapin sa kahit anong bagay. Kakampi mo ko bes! Aja! Luv u happy birthday beshy 💚"},
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