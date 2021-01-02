<template>
  <div id="menu-card">
    <b-container>
      <b-row align-v="center">
        <b-col md="4">
          <b-card
                  :title="name"
                  img-src="https://picsum.photos/600/300/?image=25"
                  img-alt="Image"
                  img-top
                  tag="article"
                  style="max-width: 20rem;"


          >
            <b-card-text v-text="description">
              <!--          Some quick example text to build on the card title and make up the bulk of the card's content.-->
            </b-card-text>

            <b-button href="#" variant="primary">Go somewhere</b-button>
          </b-card>
        </b-col>
      </b-row>
<!--      <b-row>-->
<!--        <b-col>-->
<!--          <b-col md="4">-->
<!--            <b-card-->
<!--                :title="name"-->
<!--                img-src="https://picsum.photos/600/300/?image=25"-->
<!--                img-alt="Image"-->
<!--                img-top-->
<!--                tag="article"-->
<!--                style="max-width: 20rem;"-->


<!--            >-->
<!--              <b-card-text v-text="description">-->
<!--                &lt;!&ndash;          Some quick example text to build on the card title and make up the bulk of the card's content.&ndash;&gt;-->
<!--              </b-card-text>-->

<!--              <b-button href="#" variant="primary">Go somewhere</b-button>-->
<!--            </b-card>-->
<!--          </b-col>-->
<!--        </b-col>-->
<!--        <b-col>2 of 3</b-col>-->
<!--        <b-col>3 of 3</b-col>-->
<!--      </b-row>-->

    </b-container>

  </div>

</template>

<script>
export default {
name: "HomeMenu",
  props:['id', 'name', 'description'],
  data(){
  return{
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
  /*display: flex;*/
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.26);
  margin: 1rem;
  border-radius: 10px;
  padding: 1rem;
  /*text-align: center;*/
}
</style>