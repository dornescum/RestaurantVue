<template>
  <section id="menu-card">
    <b-container>
      <b-row align-v="center">
        <b-col>
          <b-card
              :title="name"
              :img-src="img"
              img-alt="Image"
              img-top
              tag="article"
              :footer="chef"
          >
            <b-card-text v-text="description">
              <!--          Some quick example text to build on the card title and make up the bulk of the card's content.-->
            </b-card-text>


          </b-card>
        </b-col>
      </b-row>
    </b-container>
  </section>


</template>

<script>
export default {
  name: "HomeMenu",
  props: ['id', 'name', 'description', 'img', "chef"],
  data() {
    return {
      // menuItems: [{
      //   id:1, name:'some food',
      //   textDescription: `Lorem ipsum dolor sit amet, consectetur adipisicing elit. In optio recusandae veritatis. Aliquam asperiores consequatur laboriosam natus odio, reiciendis voluptatem!`
      // }]
    }
  }
}
</script>

<style scoped>

#menu-card {
  display: flex;
  flex-direction: row;
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.26);
  margin: 1rem;
  border-radius: 10px;
  padding: 0.5rem;
  text-align: center;
  background-color: var(--clr-grey-10);

}
@media (max-width: 1600px) {
  #menu-card {
    font-size: 16px;
    padding:12px 8px;
    /*background-color: green;*/

  }
}

@media (max-width: 1200px) {
  #menu-card {
    font-size: 16px;
    padding:12px 8px;
    /*background-color: red;*/
  }
}
@media (max-width: 800px) {
  #menu-card {
    font-size: 14px;
    padding:12px 8px;
  }
}
</style>