<template>
  <v-app class="index">
    <form
      class="form"
    >
      <v-row>
        <v-col cols="12" md="12" sm="12">
          <h2 class="text-font">About</h2>
          <h3 class="about-text" style="">Law Firm Overview</h3>
          <v-row class="mt-5">
            <v-col cols="12" md="6" sm="6" class="px-5 py-5">
              <p>
                Our Law Firm handles personal injury cases. The firm has been functioning for more
                than 20 years and has provided high-quality legal advice to victims of accidents. We
                take clients involved in any type of accident.
              </p>
            </v-col>  <v-col cols="12" md="6" sm="6" class="px-5 py-5">
              <p>
                Our Law Firm handles personal injury cases. The firm has been functioning for more
                than 20 years and has provided high-quality legal advice to victims of accidents. We
                take clients involved in any type of accident.
              </p>
            </v-col>
          </v-row>

        </v-col>
      </v-row>
    </form>
    <div class="btn2" style="">
      <v-btn
        class="batten2"
      >
        OUR TEAM
      </v-btn>
      <v-btn
        class="batten2"
      >
        JOIN TEAM
      </v-btn>
    </div>
  </v-app>


</template>


<script>

export default {
  data() {
    return {
      projects: [
        {
          title: "  Our Law Firm handles personal injury cases. The firm has been functioning for more\n" +
            "              than 20 years and has provided high-quality legal advice to victims of accidents. We\n" +
            "              take clients involved in any type of accident."
        }
      ],
      items: [
        {
          title: "  Our Law Firm handles personal injury cases. The firm has been functioning for more\n" +
            "              than 20 years and has provided high-quality legal advice to victims of accidents. We\n" +
            "              take clients involved in any type of accident."
        },
      ]
    }
  },
  components: {}
}
</script>
<style>
.index {
  background-image: url("https://www.thewowstyle.com/wp-content/uploads/2015/01/nature-images.jpg") !important;
  background-repeat: no-repeat !important;
  background-size: cover !important;

}

.text-font {
  font-size: 40px;
}
.about-text{
  padding-top: 10px;
  font-size: 50px
}

@media (max-height: 900px) {
  .form {
    padding-left: 5% !important;
    padding-top: 5% !important;
    height: auto !important;
  }

  .text-font {
    text-align: center;
    font-size: 40px;
  }

  .btn2 {
    padding-left: 250px !important;
  }

}

@media (max-width: 1300px) {
  .about-text{
    font-size: 30px;
  }

  .btn2 {
    padding-left: 90px !important;
  }

  .title1 {

  }
}

.btn2 {
  margin-top: 20%;margin-left: 10%;
}

.batten2 {
  border-radius: 20rem;
  text-transform: uppercase;
  border: 1px solid white;
  box-shadow: none;
  width: 150px;
  transition: all 0.5s ease-in-out;
  background-color: transparent !important;


}

.form {
  padding-top: 40px;
  padding-left: 70px;
  background: rgba(190, 104, 107, 0.9);
  height:auto;
}

.batten2:hover {
  background-color: white !important;
  color: black;
}

.title1 {
  padding-left: 40px;
}
</style>
