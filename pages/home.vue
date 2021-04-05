<template>
  <v-app style="background-color: lightcoral" class="px-8">
    <transition
      name="route"
      mode="out-in"
    >

      <div class="col-md-4 col-ms-4">
        <p class="home-page-p">LAW FIRM</p>
        <h1 class="text1">PERSONAL ATTORNEYS</h1>
        <p
        style="padding-top: 190px; padding-left: 100px"
        >
          © COSPO, 2016
        </p>

      </div>

    </transition>

  </v-app>
</template>
<style>
.home-page-p {
  font-size: 20px;
  padding-top: 280px;
  padding-left: 100px;
}

@media (max-height: 900px){
.home-page-p{
  padding-top: 50px;
}
  .text1{
    font-size: 60px;
  }
}
@media (max-width: 1300px) {
.home-page-p{
  padding-top: 200px;
  padding-left: 0;
}


  .text1 {
    margin-left: 0!important;
    font-size: 50px;
  }

}
h1 {
  font-size: 4.857rem;
  line-height: 1.08;
  margin-bottom: .58em;
  margin-top: .55em;
}

.text1 {
  padding-top: 50px;
  margin-left: 100px;
}

.route-enter, .route-leave-to {
  opacity: 0;
  transform: translateY(4em);
}

.route-enter-active, .route-leave-active {
  transition: all 1s ease;
}

</style>
<script>
import Contact from "@/pages/contact";
export default {
  components: {Contact}
}
</script>
