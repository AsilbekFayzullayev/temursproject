<template>
  <v-app class="index-main">
    <form
      class="index-padding"
    >
      <h1 class="faq-text">FAQ</h1>
      <v-expansion-panels  style="padding-top: 30px; width: 1000px">
        <v-expansion-panel
          class="razmer"
          v-for="project in projects"
          :key="project.title"

          style="background: rgba(190, 104, 107, 0.4); padding-top: 10px">
          <v-expansion-panel-header>
            {{ project.title }}
          </v-expansion-panel-header>
          <v-expansion-panel-content>
            {{ project.person }}
          </v-expansion-panel-content>
        </v-expansion-panel>
      </v-expansion-panels>
    </form>
  </v-app>
</template>

<script>
export default {
  name: "faq",
  data() {
    return {
      projects: [
        {title: 'WHO IS "ITEMBRIDGE"?', person: 'Our company is the friendly team of professionals, who offers a number of creative products, such as online stores, templates, one page promo sites, graphic works and corporate style for the wide audience.'},
        {title: 'WHAT DOES "ITEMBRIDGE" COMPANY DO?', person: 'The company owns its success to the friendly team of professionals, who create exclusive designs, unique and clear functionality of the templates. Corporate style and graphic works always have the perfect design so you do not have to change a lot of settings to achieve the desired style.'},
        {title: 'WHAT IS OUR MISSION?', person: 'Our company is the friendly team of professionals, who create exclusive designs, unique and clear functionality of the templates. Corporate style and graphic works always have the perfect design so you do not have to change a lot of settings to achieve the desired style.'},
        {title: 'WHAT PRODUCTS DOES THE COMPANY PRODUCE?', person: '"Itembridge" produces exclusive creative products such as online stores templates, one page promo sites, graphic works and corporate style for the wide audience. All they are of high quality.'},
        {title: 'HOW DID THE COMPANY BECAME FAMOUS?', person: '"Itembridge" is a company, that became famous among thousands of visitors and purchasers of the most known online resource copyright works during the short period of its existence.'},
        {title: 'WHAT IS THE TEAM OF "ITEMBRIDGE" COMPANY?', person: '"Itembridge" is a team of talented people with big ideas and creative minds. We develop exclusive designs, unique, easy and clear functionality of the products. We are a team of young professionals who are always open to new knowledge.'},
      ]
    }
  }
}
</script>

<style scoped>

.index-main {
  background-image: url("https://www.benq.eu/content/dam/b2c/en-us/knowledge-center/how-do-i-make-sure-netflix-streams-in-4k/Netflix_in_4K.png");
  background-size: cover;
  max-width: 100%;
  height: auto;

}

@media (max-width: 1300px) {
  .index-main{
    background-image: url("https://www.benq.eu/content/dam/b2c/en-us/knowledge-center/how-do-i-make-sure-netflix-streams-in-4k/Netflix_in_4K.png")

  }
  .faq-text{
    text-align: center;
    font-size: 40px;
  }
  .index-padding{
  padding-left: 10px!important;

  }
}
.razmer{
  box-shadow: none!important;
  width: 0!important;
  text-transform: uppercase;
}
.index-padding{
  padding-top: 70px;
  padding-left: 70px;
  background: rgba(190, 104, 107, 0.9);
  height: 100%;
  width: 100%;
}
</style>
