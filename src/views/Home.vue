<template>
  <div class="home">
    <HelloWorld/>
    <section id="foodItems">
      <HomeMenu
          v-for="item in menuItems" :key="item.id"
          :name="item.name"
          :description="item.textDescription"
      ></HomeMenu>
    </section>
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue'
import HomeMenu from "@/components/HomeMenu";

export default {
  name: 'Home',
  components: {
    HelloWorld,
    HomeMenu
  },
  data() {
    return {
      menuItems: [
        {
          id: 1, name: 'some food1',
          textDescription: `Lorem ipsum dolor sit amet, consectetur adipisicing elit. In optio recusandae veritatis. Aliquam asperiores consequatur laboriosam natus odio, reiciendis voluptatem!`
        },
        {
          id: 2, name: 'some food2',
          textDescription: `Lorem ipsum dolor sit amet, consectetur adipisicing elit. In optio recusandae veritatis. Aliquam asperiores consequatur laboriosam natus odio, reiciendis voluptatem!`
        },
        {
          id: 3, name: 'some food3',
          textDescription: `Lorem ipsum dolor sit amet, consectetur adipisicing elit. In optio recusandae veritatis. Aliquam asperiores consequatur laboriosam natus odio, reiciendis voluptatem!`
        },
        {
          id: 4, name: 'some food4',
          textDescription: `Lorem ipsum dolor sit amet, consectetur adipisicing elit. In optio recusandae veritatis. Aliquam asperiores consequatur laboriosam natus odio, reiciendis voluptatem!`
        },

      ]
    }
  }
}
</script>
<style>
#foodItems {
  /*display: flex;*/
}
</style>
