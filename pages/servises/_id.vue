<template>
  <form class="form1">
    <h2  style="font-size: 40px ">
      {{ this.$store.state.item.inside_data.title }}
    </h2>
    <span>
      {{ this.$store.state.item.inside_data.text }}
    </span>
    <p>
    <v-img  class="photo1"  :src="this.$store.state.item.inside_data.src">

    </v-img>
    </p>
   <p style="margin-top: 150px!important;">
     {{ this.$store.state.item.inside_data.text }}
   </p>
  </form>
</template>

<script>
export default {
  name: "_id",
  created() {
    console.log(this.$store.state.item.inside_data.src)
  }
}
</script>

<style scoped>
@media (max-width: 1300px) {
  .photo1{
    left: 0!important;
    width: 368px!important;
  }
  .form1{
    padding-top: 70px;
    padding-left: 4px!important;
    background: rgba(190, 104, 107, 0.8);
  }
}
.form1{
  padding-top: 70px;
  padding-left: 70px;
  background: rgba(190, 104, 107, 0.8);
  height: 1100px;
  width: 100%;
}
.photo1{
  left: 200px;
  top: 100px;
  width:900px;
  height:660px
}
</style>
