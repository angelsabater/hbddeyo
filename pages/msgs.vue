<template>
  <v-layout align-center column fill-height>
    <v-flex text-center>
      <v-card width="800px">
        <v-container>
          <v-layout column>
            <v-flex
              v-for="n in messages"
              :key="n"
              xs6
              my-4
            >
              <v-card flat tile class="d-flex">
                <v-layout>
                  <v-flex xs4>
                    <v-img
                      :src="n.src"
                      :lazy-src="`https://picsum.photos/10/6?image=${n * 5 + 10}`"
                      aspect-ratio="1"
                      class="grey lighten-2"
                      style="border-radius: 5%"
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
                      {{n.message}}
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

<script>
  export default {
    data () {
      return {
        messages: [
          {message: "Happy Birthday Tura! Wish you all the best. Goodluck sa career pero tangina dapat may swimming pa din dapat tayo tsaka christmas party ahahahaha. Yun lang. Advance salamat sa libre nyo hehe 😄", 
          src:"https://scontent-nrt1-1.xx.fbcdn.net/v/t1.0-9/61564265_2318089924950431_1715318940550299648_n.jpg?_nc_cat=108&_nc_oc=AQkq_FSfVaYha9Co8zILq2ZBQpU5LaPAByvoVD9XokFSrc-HZrINTphFRnp3hMhN654&_nc_ht=scontent-nrt1-1.xx&oh=67fef161796697a8d1a50ff8312b297c&oe=5DA3B0D6"},
          {message: "Happy borkday deyss level 21 ka na HAHAHA naks bilis magpalevel penge naman ng tips labyu 😘 -Jason",
          src:"https://scontent-nrt1-1.xx.fbcdn.net/v/t1.0-9/12642508_1107959615894338_2078157610332352726_n.jpg?_nc_cat=104&_nc_oc=AQm4-4Xh6h6flIB0FJqHj9GNzOPktZvtnXk3uvi-37ARcGx4BQH1XR3I_0BmE1MT3zg&_nc_ht=scontent-nrt1-1.xx&oh=72915a923fed00978219bf14b1cef004&oe=5DDC1732"},
          {message: "UYY DEYOO HAPPY BIRTHDAAY KAHIT WALA NA TAYONG MASHADONG BONDING DI MO PARIN NAKAKALIMUTAN YUNG NAZARENO NIYO HAHAHAHAHAHA CHOS PERO AYUN HAPPY BIRTHDAY DEYO INGAT KA PALAGI ALAM KO NAMAN NA KAYA MO ANG LYF HAHAHAHAHA ETNEB LANG SA UMAGA AT GABI PARA MAY TAKWARENTS KA KICKBACK KA NA LANG NG PUSAM MAY TASINGKWENT KA NA HAHAHAHAHA AYUN GOOD LUCK SA BUHAY SANA NAEENJOY MO WORK MOO YIEEEE LABYU DEYO HAPPY BORTHDOOOY -Julius",
          src: "https://scontent-nrt1-1.xx.fbcdn.net/v/t1.0-9/12509308_1126462170699357_830006950173846507_n.jpg?_nc_cat=110&_nc_oc=AQkbWgLX0KkgbK5SKIhZYxhld4QJGqoM0nAyO2KCqkg4dOazzniV3mkrFoiIZyX6N3k&_nc_ht=scontent-nrt1-1.xx&oh=567cba494c6c81e5aa664179a169120e&oe=5DCF9AC2"},
          {message: "Happiest birthday to my numbah one bestie!!! 😜 Brace yourself hahabaan ko to, kasi may work ka na 💸hahahaha. First of all, sobrang thankful ako kay Lord kasi binigyan nya ko ng “Deo”. I know ginawa ka talagang instrument ni Lord to be a blessing to others. wag ka kiligin di pa tapos Thank you kasi lagi kang nandyan for me mapa ups and downs, LEGIT. Though not in person pero isang call or chat lang g ka agad. Thank you kasi sobrang supportive mo 💯 and lagi kang open to listen sa lahat ng rants ko sa life. And lastly, thank you kasi di ka nagbago at nagsawa kahit sobrang gaga ko. Ops 🙊 Basta andito lang din ako lagi for you, alam mo yan!!! Sana magkaron din tayo ng time mag worship ulit together hehe miss you! 🙏🏻 Uhm, sa lovelife? Hahaha ano ba? Pinagppray ko na sya dont worry hahaha dadating din sya bes enjoyin mo lang ung time mo muna with yourself and your fam. 💞 Pineprepare ka lang ni Lord. Basta wag mo ko ssnob-in pag dumating yon ha 💪🏻 Sa career, yan na nagsstart ka na and I know there’s more to come! Deserve na deserve mo yan!! 🤗 Once again, happy birthday rico!! I hope you’ll have a wonderful day! Godbless! Love you!! ❤️ -Jillean", 
          src:"https://scontent-nrt1-1.xx.fbcdn.net/v/t1.15752-9/67814921_393220324504503_5917927697903779840_n.jpg?_nc_cat=103&_nc_oc=AQk5ocxZwEUG2SEe709JeUrUFdC08sIOBSjONcesKw8N0XLxlUQC0j0mOxcmhev8xqo&_nc_ht=scontent-nrt1-1.xx&oh=1e7ab6d4c0a218ac1360ee090689f0a6&oe=5DD957C8"},
          {message: "Happy Bornday turs isa ka pa bilis mo magpalevel ha hahaha labyu 😘 -Jason", 
          src:"https://scontent-nrt1-1.xx.fbcdn.net/v/t1.0-9/1380414_1116859801670986_3392169873825391094_n.jpg?_nc_cat=111&_nc_oc=AQkMr6bD8NX9QxG22Jqe4NAC8lCm3pcvOdeCFUN_735jMSEqH97zj_WOc35INOl2DDU&_nc_ht=scontent-nrt1-1.xx&oh=17dcc72cb7d0e2cbaa59d70cb44a9029&oe=5DA5A6F5"},
          {message: "Happy birthday svg brother Deyo. Sana mahanap mo na yung babaeng para sayo bukod kay Mika. Stay busog as always! 🤣 -Jro", 
          src:"https://scontent-nrt1-1.xx.fbcdn.net/v/t1.15752-9/67738429_471695646721272_9067799718574161920_n.jpg?_nc_cat=101&_nc_oc=AQnUZr9AWhYHakZLQazMSbMqCl9qJqIUQj7idYbtg2FU3icaFJHYBofpfvHaAUp_ZlY&_nc_ht=scontent-nrt1-1.xx&oh=3a34dfc104cf2ff77f3e3dd81716a6dc&oe=5DE3B6E9"},
          {message: "Alam kong matagal mo ng inaadmire yung bangs ko at matagal mo ng pinapangarap na sana magkaron ka non at baka nga di ka pa makatulog kasi nangagati na noo mo kaya pinagedit na kita. Wag ka ng malungkot kasi kasama mo pa rin naman jan si sabater eh.Happy Birthday Deyo!!! -Poch",
          src:"https://scontent-nrt1-1.xx.fbcdn.net/v/t1.15752-9/68449153_2133164663648870_4626737787150794752_n.jpg?_nc_cat=106&_nc_oc=AQntxeq6o6H7ljFTG5jVF05eicObMMk9se6E4vvp8ObMErj8X_DtwfS6CL18WcfOcTI&_nc_ht=scontent-nrt1-1.xx&oh=5f47d41da91c74042071085b47c6f021&oe=5DE872D9"},
          {message: "TURAAAA!! KAMUSTA NA WORK MO JAN? HAHAHA PAPATAYIN KA NA BA? NAGWORK KA LANG JAN NAGKAJOWA KA NA HHAHAHAHAHA PUPET MO NAMAN PO MASTER HAHAHAHA PERO AYUN HAPPY BIRTHDAY TURA I KNOW YOU ARE DOING UR BEST KAHIT SAAN SAAN NA KAYO PINAPADALA NI ANTON PARA KAYONG MAY CONCERT EH HAHAHAHA TURA WORLD TOUR MALAPIT MO NA MALIBOT PILIPINAS HAHAHAHAHA INGAT PALAGI HA ALAGAAN ANG SARILI PARA DI MAGKASAKIT GOOD LUCK SA CAREER NIYOOO LABYUUUU -Julius",
          src:"https://scontent-nrt1-1.xx.fbcdn.net/v/t1.0-9/12642586_1111969618826671_8271614112703601346_n.jpg?_nc_cat=100&_nc_oc=AQmEiFe2WI5Bo1UYdh7RVcn9IRu41Ik7e9K2hfqT8ER89nZQAMzcuuuGChXK25zCZFg&_nc_ht=scontent-nrt1-1.xx&oh=f27f0b3c85dd63af5ecd9220d40806ba&oe=5DCEEF32"},
          {message: "hi deyoooooo ✨ happy happy birthday! i wish you nothing but success in your career. Good luck on your future endeavors! I know you’ll do great! 😊 May God bless you more everyday because i know you deserve it! Happiest Birthday Deyoooo! I hope you enjoy your day! 💫 -Iyaih",
          src: "https://scontent-nrt1-1.xx.fbcdn.net/v/t1.15752-9/67565131_517961825620292_3484563544848990208_n.jpg?_nc_cat=103&_nc_oc=AQnTFWzxWI-ioUhoKn_6pAtweZG7QEuwVkbnBw6UP7Kiac2kHlR8BA34tzqBt_V1xbY&_nc_ht=scontent-nrt1-1.xx&oh=b4938eb5396c9f34a43463dc2a3fefac&oe=5DE36851"},
          {message: "HABADUU DEYOOO ADEL Naway pag palain ka ng Panginoon. Mag iingat at mag enjoy ka lang sa path na gusto mo tahakin. Tsaka yung unan na binigay mo ay ginagamit ko pa din as strength. Salamat sa panahon ng pag eencourage. I love you so much. The Lord bless you and ganun din sa iyong pamilya - Doms",
          src:"https://scontent-nrt1-1.xx.fbcdn.net/v/t1.0-9/12799382_1151235388222035_8588880598036499234_n.jpg?_nc_cat=110&_nc_oc=AQl9z_m1JV-eUc2GdODXCSthw8E9XOGSi-TFOLxnRMKdkp3h4uDzRdb8-WdAzeD9mig&_nc_ht=scontent-nrt1-1.xx&oh=a1fde345207487f5b758ff8aafd02019&oe=5DE501BB"}, //doms
          {message: "Happy Birthday kuya deydey! HAHAHAHA di na kuya pa tito na 😅 thankyou for being a good friend back in our college days (kala mo tagal na e hahaha) Stay awesome! Hahahaha goodluck on your future endeavors! Wag po makalimot pag boss na hahahaha mbtc & Godbless! 🙏🥰💗 -Mickie",
          src:"https://scontent-nrt1-1.xx.fbcdn.net/v/t1.15752-9/68265714_2367598346659189_7857988808036319232_n.jpg?_nc_cat=104&_nc_oc=AQk5VWUjyA-vkDGZLL1ffM6X6Y6zurPYNLasWRwm5-O6Ntuwu355UlXYOQqZOR79v6s&_nc_ht=scontent-nrt1-1.xx&oh=d4576971ae1cdae365e768724d0f9a9f&oe=5DD819E3"}, //mickie
          {message: "Hello Deo, happy happy birthday ☺ I hope you enjoy your day. I miss you and your squad hehe kakamiss yung mga panahong kasama namin kayo sa SC. I just want to thank you pala kahit medyo late na dahil kahit na naging magkalaban tayo dati sa SC, hindi tayo nakaramdam ng awkwardness sa isa't isa after. Thank you sa pagtulong sa SC noon. Alam nyo naman na love ko kayo hehe more blessings to come and hoping you a successful career in the future. Ingat lagi!!!! See you soon 🤗 -VP",
          src:"https://scontent-nrt1-1.xx.fbcdn.net/v/t1.15752-9/67708050_500363000728689_5961605982000775168_n.jpg?_nc_cat=104&_nc_oc=AQnxIj8eGKgvfCO4RRru2gEp6z-Ni8ALVt0ZLBGB_uqrcwEmJrS1Q0B2Ccpl4NjRnWU&_nc_ht=scontent-nrt1-1.xx&oh=c48c2540887a9d3e5472f403d545435f&oe=5DE74559"}, //vp
          {message: "Happy Birthday Kuya Deyooooo. Stay what you are, see you soon 💕 kahit di tayo masyado nagkakakwentuhan never ka naging snobber hahhahaha. Goodluck and God bless you 😊 - Dane",
          src:"https://scontent-nrt1-1.xx.fbcdn.net/v/t1.0-9/12002878_1070174562994785_8267492140004082270_n.jpg?_nc_cat=101&_nc_oc=AQlD4I1vL5r4IYvOcYWNFtRqlV8a9wHmV5nxiN3WePk3G2K6ABbPUrE1TYUJ7Ezw_P8&_nc_ht=scontent-nrt1-1.xx&oh=d9f1b9063c5cd7438fb9d9216e5fb201&oe=5DD46169"}, //dane
          {message: "Happy Birthday, Deo. Ate is so proud sa lahat ng achievements mo. I’ve seen you ever since totoy days mo pa lang so in short nakita ko how sipag you are since hs and college days. Pagpatuloy mo lang ang pagsisipag sa lahat ng bagay kasi may magandang blessings na kapalit yan. May God bless you more and enjoy your day. -Ate Kim",
          src:"https://scontent-nrt1-1.xx.fbcdn.net/v/t1.15752-9/68260025_852118521826379_6146759380726448128_n.jpg?_nc_cat=108&_nc_oc=AQkVTJq6HjyUgvvZxElOgw1Rd_NSmkaYH_7y-6SXfW1J0nHf6mp1hPuRB9crfIpy8-A&_nc_ht=scontent-nrt1-1.xx&oh=eb9125dc30e32749c814c7103700a788&oe=5DA0ED52"}, //ate kim
          {message: "DEYO DEYO DEYO HAPPY HAPPY BIRTHDAY!!!! Miss you 😘 miss na din kita yakapin 🤗🤗 mbtc love love ❤❤ - Jade",
          src:"https://scontent-nrt1-1.xx.fbcdn.net/v/t1.15752-9/s2048x2048/67688116_437124190214271_4606481316928552960_n.jpg?_nc_cat=101&_nc_oc=AQkmtB7gqS-AkgHENKCnFgi35eS6bge_Nmmsw1auPf4bRYYLZc9AonLoACOaPETFEgA&_nc_ht=scontent-nrt1-1.xx&oh=23d1573dd7d401af22ab4f63667ef660&oe=5DEA1448"}, //jade
          {message: "(nagsend lang si Bea ng picture, di ka nya binati HAHAHAHAHAHA)",
          src:"https://scontent-nrt1-1.xx.fbcdn.net/v/t1.15752-9/67475781_454823088703704_3465460007057752064_n.jpg?_nc_cat=105&_nc_oc=AQlCHUFPnZwD5YPiurIFejZPGuCNwV4L9fTc1ZOpPIifIMI6xkdV1w3-22qOstt0Yts&_nc_ht=scontent-nrt1-1.xx&oh=6e3b2275a8b04f430d9533d17569f77d&oe=5DDF0A0B"},
          {message: "Happy birthday deyo!!! Napaka-panget mo!!!! Samgyup na us?! CHE BALAKAJAN LABYU MWA HAHAHAHAH -Erick",
          src:"https://scontent-nrt1-1.xx.fbcdn.net/v/t1.15752-9/67821278_2903741749851432_8987199090987106304_n.jpg?_nc_cat=109&_nc_oc=AQmeRJTwlbQLoLaewZllAzKJH4jVTJzIV0xCiT-__kdwE4vrv3E7Rjni8L9zJsITU1w&_nc_ht=scontent-nrt1-1.xx&oh=d061624c6742db057dfd7476e98ce8d5&oe=5DE30148"},
          {message: "Happy birthday Deyo/G5/Baymax/baboy/panget!! HAHAHA Thank you nga pala kanina. Sana natuwa ka sa simpleng sulat namin sayo. Thank you din sa mcdo. Lol salamat sa friendship. Alam mo nayan. Putek. Nasa letter na lang. Goodluck sa college! Stay panget jk. Stay mabait at masipag...at mabait uli. HAHA ge gwapo na. Ok daldal. Andito lang kaming '⚡️' para sayo. Ilurvyouuuu!!! -ayan yung message ko 4years ago. HAHAHAHAHAHAH happyy birthday!! Tara night swimming na. Miss ko na kayo 😞 love u alwayss. 💕 -She",
          src:"https://scontent-nrt1-1.xx.fbcdn.net/v/t1.15752-9/67822362_715847275509535_2823408232196734976_n.jpg?_nc_cat=102&_nc_oc=AQlYw_V1Gu-w0EyqkJuEBI7NpxCOgE32bPNYM4sHemLcj6ABG4sBvMK28a3xZFbdOzg&_nc_ht=scontent-nrt1-1.xx&oh=6d828b1e2513eb600f35814f44a3a3a4&oe=5DD520C9"},
          {message: "Happy birthday, Deyo! I wish you all the best in life—career, health, love life, everything. I wish we could've gotten to hang out more back then. Pero soon! Pag umuwi ako! Haha. I hope you enjoy your day! Keep being a sunshine, asset mo yan, lol. Ingat lagi, and God bless! -Mica",
          src:"https://scontent-nrt1-1.xx.fbcdn.net/v/t1.15752-9/s2048x2048/67968154_1112947062234203_4191244016190226432_n.jpg?_nc_cat=106&_nc_oc=AQkP7oznude3tAtpUmc2TuMtOKYWuiWxBc07yV5IQmmfEAM80Kz2-wmfV_j3CtIkE6M&_nc_ht=scontent-nrt1-1.xx&oh=f87f97f7f8ad65f5e4af9d89497f9c0c&oe=5DD2B217"},
        ]
      }
    },
  }
</script>