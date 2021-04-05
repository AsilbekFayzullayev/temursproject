<template>
  <v-app class="mine-index">
    <form
      class="text2"
    >
      <h1 class="services-text">SERVICES</h1>
      <P>
        Lorem ipsum dolor sit amet, consectetur adipisicing elit. Animi atque commodi culpa, debitis doloremque eaque
        est perspiciatis totam vitae.
        Ab asperiores aspernatur deserunt doloribus error ipsa mollitia perspiciatis qui rerum!
      </P>
      <v-list-item-group
        text
      >
        <v-list-item
          @click="selectItem(item)"
          v-for="(item, i) in items"
          :key="i"
        >
          <v-list-item-icon>
            <v-icon v-text="item.icon"></v-icon>
          </v-list-item-icon>
          <v-list-item-content>
            <v-list-item-title v-text="item.text"></v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list-item-group>
    </form>
  </v-app>
</template>

<script>
export default {
  selectedItem: 1,
  name: "services",
  data() {
    return {
      items: [
        {
          id: 1, text: 'ONLINE CONSULTATION', icon: 'mdi-camera',
          inside_data: {
            title: "PANORAMIC NATURE",
            text: "The firm has been functioning for more than 20 years and has provided high-quality legal advice to victims of accidents.\n" +
              "\n" +
              "Our Law Firm handles personal injury cases. The firm has been functioning for more than 20 years and has provided high-quality legal advice to victims of accidents. We take clients involved in any type of accident.",
            src: "https://images.unsplash.com/photo-1554080353-a576cf803bda?ixid=MXwxMjA3fDB8MHxzZWFyY2h8MXx8cGhvdG98ZW58MHx8MHw%3D&ixlib=rb-1.2.1&w=1000&q=80"
          }
        },
        {
          id: 2, text: 'CIVIL RIGHTS', icon: 'mdi-wallet-travel',
          inside_data: {
            title: "CIVIL RIGHTS",
            src: "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQmXxB47SU38PnAvZp23sdr27t8JNvIjvIV7g&usqp=CAU",
            text: "We understand that the injury can change people's lives. That's why we help people to cope with the trauma of the accident and stand by throughout the process\n" +
              "\n" +
              "Our Law Firm handles personal injury cases. The firm has been functioning for more than 20 years and has provided high-quality legal advice to victims of accidents. We take clients involved in any type of accident."
          }
        },
        {
          id: 3, text: 'ASSURANCE', icon: 'mdi-image',
          inside_data: {
            title: "ASSURANCE",
            text: "We take clients involved in any type of accident. We do what is necessary to allow clients to get a fair compensation.\n" +
              "\n" +
              "Our independent professional service has a goal to improve the clients' lifes and reduce the risk of incorrect information. We are a legal organization avoiding problems when delivering solutions to customers.\n" +
              "\n",
            src: "https://swordstoday.ie/wp-content/uploads/2020/11/From-June-1-2021-Google-Photos-will-no-longer-offer.jpg"
          }
        },
        {
          id: 4, text: 'TRADE REGULATION', icon: 'mdi-toggle-switch-off-outline',
          inside_data: {
            title: "TRADE REGULATION",
            src: "https://images.unsplash.com/photo-1550041771-aef92f14a6d5?ixid=MXwxMjA3fDB8MHxzZWFyY2h8Mjh8fGRvd25sb2FkfGVufDB8fDB8&ixlib=rb-1.2.1&w=1000&q=80"
            ,
            text: "Our Law Firm handles personal injury cases. We understand that the injury can change people's lives. We take clients involved in any type of accident.\n" +
              "\n" +
              "We specialize in this field of law, including government regulation of unfair methods of competition and unfair or deceptive business acts or practices. Antitrust law is often considered a subset of trade regulation law. Franchise and distribution law, consumer protection law and advertising law are sometimes considered parts of trade regulation law."
          }
        },
        {
          id: 5, text: 'BANKRUPTCY', icon: 'mdi-credit-card-outline',
          inside_data: {
            title: "BANKRUPTCY",
            src: "https://pub-static.fotor.com/static/web/site/features/blur/images/features-featurecard-ColorSplash-en-a.jpg"
            ,
            text: "The firm has been functioning for more than 20 years and has provided high-quality legal advice to victims of accidents.\n" +
              "\n" +
              "Our Law Firm handles personal injury cases. The firm has been functioning for more than 20 years and has provided high-quality legal advice to victims of accidents. We take clients involved in any type of accident."
          }
        },
        {
          id: 6, text: 'CRIMINAL LAW', icon: 'mdi-message-processing-outline',
          inside_data: {
            title: "CRIMINAL LAW",
            src: "https://images.unsplash.com/photo-1554080353-a576cf803bda?ixid=MXwxMjA3fDB8MHxzZWFyY2h8MXx8cGhvdG98ZW58MHx8MHw%3D&ixlib=rb-1.2.1&w=1000&q=80"
            ,
            text: "We take clients involved in any type of accident. We do what is necessary to allow clients to get a fair compensation.\n" +
              "\n" +
              "We understand that the injury can change people's lives. That's why we help people to cope with the trauma of the accident and stand by throughout the process. We do what is necessary to allow clients to get a fair compensation."
          }
        },
      ]
    }
  },
  methods: {
    selectItem(item) {
      this.$store.state.item = item
      this.$router.push(`servises/${item.id}`)
    }
  }

}
</script>

<style scoped>
.mine-index {
  background-image: url("https://royalbcmuseum.bc.ca/sites/default/files/images/basic-pages/galleries/8952443104_808727392c_o.jpg");
  background-repeat: no-repeat;
  background-size: cover;
}

@media (max-width: 1300px) {
  .services-text{
    text-align: center;
    font-size: 50px;
  }
  .text2 {
    padding-left: 20px;
  }
}

.text2 {
  padding-top: 70px;
  padding-left: 50px;
  background: rgba(190, 104, 107, 0.9);
  height: 100%;
  width: 100%;
}
</style>
