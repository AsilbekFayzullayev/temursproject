<template>
  <v-app class="navigationdiv">
    <form
      class="form5"
      style="
      background: rgba(190, 104, 107, 0.9);
      height: 100%;
      width: 100%;
">
      <v-row class="text-center py-5">
        <v-col cols="12" md="2" sm="2" class="pster">
          <v-img width="60" height="60" class="mt-10 ml-10 py-10 px-10 icon" style="" v-for="(item,i) of items "
                 :key="i" :src="item.icon"
                 @click="select(item)"
          ></v-img>
        </v-col>
        <v-col cols="12" md="10" sm="10">
          <v-row>
            <v-col md="12" class="px-16 people" >
              <h1 class="people-text">WHAT PEOPLE SAY?</h1>
              <v-img :src="selectedItem.src" class="people-photo"></v-img>
            </v-col>
            <h4>{{ selectedItem.text }}</h4>
          </v-row>

        </v-col>
      </v-row>


      <!--      <v-row align="center">-->
      <!--        <v-item-group-->
      <!--          v-model="window"-->
      <!--          class="item_group"-->
      <!--          tag="div"-->
      <!--        >-->
      <!--          <v-item-->
      <!--            v-for="n in items"-->
      <!--            :key="n"-->
      <!--            v-slot="{ active, toggle }"-->
      <!--          >-->
      <!--            <div>-->
      <!--              <v-btn-->
      <!--                :input-value="active"-->
      <!--                icon-->
      <!--                @click="toggle"-->
      <!--              >-->
      <!--                <v-icon>mdi-record</v-icon>-->
      <!--              </v-btn>-->
      <!--            </div>-->
      <!--          </v-item>-->
      <!--        </v-item-group>-->

      <!--        <v-col>-->
      <!--          <v-window-->
      <!--            show-arrows-on-hover-->
      <!--            v-model="window"-->
      <!--            class="elevation-1"-->
      <!--            :vertical="false"-->
      <!--          >-->
      <!--            <v-window-item-->
      <!--              v-for="n in items"-->
      <!--              :key="n"-->
      <!--            >-->

      <!--              <v-card-text>-->
      <!--                <v-row-->
      <!--                  class="mb-4"-->
      <!--                  align="center"-->
      <!--                >-->

      <!--                </v-row>-->
      <!--                <h1 class="text3">-->
      <!--                  WHAT PEOPLE SAY?-->

      <!--                </h1>-->

      <!--                <v-img width="1000px" height="400px" class="photo3" :src="n.src">-->

      <!--                </v-img>-->

      <!--                <div>-->
      <!--                  <p style=" margin-top: 50px;font-size: 20px">-->
      <!--                    {{ n.text }}-->
      <!--                  </p>-->
      <!--                </div>-->
      <!--              </v-card-text>-->
      <!--            </v-window-item>-->
      <!--          </v-window>-->
      <!--        </v-col>-->
      <!--      </v-row>-->

    </form>
  </v-app>
</template>

<script>
export default {
  name: "peopleSay",
  data() {
    return {
      selectedItem: {

        text: 'Exclusive designs, unique and clear functionality of the templates are created here. The company produces exclusive creative products such as online stores templates, one page promo sites, graphic works and corporate style for the wide audience.\n' +
          'SAMANTHA THOMPSON',
        src: ("https://media.sciencephoto.com/_assets/img-pattern.jpg"),
        icon: ('http://template.cospo.itembridge.com/img/people-say/logo/light/1.svg')
      },
      items: [
        {
          text: 'Exclusive designs, unique and clear functionality of the templates are created here. The company produces exclusive creative products such as online stores templates, one page promo sites, graphic works and corporate style for the wide audience.\n' +
            'SAMANTHA THOMPSON',
          src: ("https://media.sciencephoto.com/_assets/img-pattern.jpg"),
          icon: ('http://template.cospo.itembridge.com/img/people-say/logo/light/1.svg')
        },
        {
          text: 'iphic wdience.',
          src: "http://template.cospo.itembridge.com/img/people-say/photos/2.jpg",
          icon: ('http://template.cospo.itembridge.com/img/people-say/logo/light/2.svg')

        },
        {
          text: ' They develop exclusive designs, unique, easy and clear functionality of the products. They are a team of young professionals who are always open to new knowledge. Exclusive designs, unique and clear functionality of the templates are created here.',
          src: "http://template.cospo.itembridge.com/img/people-say/photos/3.jpg",
          icon: ('http://template.cospo.itembridge.com/img/people-say/logo/light/3.svg')

        },
        {
          text: 'Distinctively revolutionize flexible methods of empowerment whereas intermandated ROI. Synergistically plagiarize next-generation resources after scalable bandwidth.Conveniently revolutionize cross-unit synergy and market positioning internal or “organic” sources. ',
          src: "http://template.cospo.itembridge.com/img/people-say/photos/4.jpg",
          icon: "http://template.cospo.itembridge.com/img/people-say/logo/light/4.svg"
        },
        {
          text: 'Distinctively revolutionize flexible methods of empowerment whereas intermandated ROI. Synergistically plagiarize next-generation resources after scalable bandwidth.Conveniently revolutionize cross-unit synergy and market positioning internal or “organic” sources. ',
          src: "http://template.cospo.itembridge.com/img/people-say/photos/5.jpg",
          icon: 'http://template.cospo.itembridge.com/img/people-say/logo/light/5.svg'
        },
        {
          text: ' Distinctively revolutionize flexible methods of empowerment whereas intermandated ROI. Synergistically plagiarize next-generation resources after scalable bandwidth.Conveniently revolutionize cross-unit synergy and market positioning internal or “organic” sources. ',
          src: "http://template.cospo.itembridge.com/img/people-say/photos/6.jpg",
          icon: 'http://template.cospo.itembridge.com/img/people-say/logo/light/6.svg'
        },
        {
          text: ' Distinctively revolutionize flexible methods of empowerment whereas intermandated ROI. Synergistically plagiarize next-generation resources after scalable bandwidth.Conveniently revolutionize cross-unit synergy and market positioning internal or “organic” sources. ',
          src: "http://template.cospo.itembridge.com/img/people-say/photos/7.jpg",
          icon: 'http://template.cospo.itembridge.com/img/people-say/logo/light/7.svg'
        },
        {
          text: 'This is a team of talented people with big ideas and creative minds. They develop exclusive designs, unique, easy and clear functionality of the products. They are a team of young professionals who are always open to new knowledge.',
          src: "http://template.cospo.itembridge.com/img/people-say/photos/8.jpg",
          icon: 'http://template.cospo.itembridge.com/img/people-say/logo/light/8.svg'
        },
        {
          text: ' This is a team of talented people with big ideas and creative minds. They develop exclusive designs, unique, easy and clear functionality of the products. They are a team of young professionals who are always open to new knowledge.,',
          src: "http://template.cospo.itembridge.com/img/people-say/photos/9.jpg",
          icon: 'http://template.cospo.itembridge.com/img/people-say/logo/light/9.svg'
        },
        {
          text: ' the friesites,',
          src: "http://template.cospo.itembridge.com/img/people-say/photos/10.jpg",
          icon: 'http://template.cospo.itembridge.com/img/people-say/logo/light/10.svg'
        },
      ],
      window: 0,
    }
  },
  methods: {
    select(item) {
      this.selectedItem = {...item}
    }
  }
}
</script>

<style scoped>
.people{
  padding-top: 60px!important;
}

.navigationdiv {
  background-image: url("https://wallpapershome.ru/images/wallpapers/park-3840x2160-5k-4k-8k-osen-listya-derevya-12400.jpg");
  background-repeat: no-repeat;
  background-size: cover;
}
.people-photo{
  height: 700px;
}
@media (max-width: 600px) {
  .people-photo{
    height: 400px;
  }
  .pster{
    display: flex;
    overflow-x: scroll;
    padding-left: 0!important;
  }
  .people-text{
    font-size: 30px;
  }

}
.pster{
  padding-left: 50px;
  background: rgba(190, 104, 107, 0.9)!important;
  opacity: .4!important;


}

.icon {
  cursor: pointer;

}

.icon:hover {
  background-color: lightcoral;

}

@media (max-width: 1300px) {
 .pster{
   padding-left: 0!important;
 }

  .form5 {
    padding-top: 30px !important;
    padding-left: 20px !important;
  }

  .text3 {
    font-size: 30px
  }

  .item_group {
    display: none;
  }
}
</style>
