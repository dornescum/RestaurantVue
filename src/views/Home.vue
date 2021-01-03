<template>
  <div>
    <HelloWorld/>
    <section id="foodItems">
      <HomeMenu
          v-for="item in menuItems" :key="item.id"
          :name="item.name"
          :description="item.textDescription"
          :img="item.img"
          :chef="item.chef"
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
          id: 1, name: 'Some food 1',
          textDescription: `Lorem ipsum dolor sit amet, consectetur adipisicing elit. In optio recusandae veritatis. Aliquam asperiores consequatur laboriosam natus odio, reiciendis voluptatem!`,
          img:"https://images.unsplash.com/photo-1504674900247-0877df9cc836?ixid=MXwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=1050&q=80",
          chef:"Ian Fraser Kilmister"
        },
        {
          id: 2, name: 'Some food 2',
          textDescription: `Lorem ipsum dolor sit amet, consectetur adipisicing elit. In optio recusandae veritatis. Aliquam asperiores consequatur laboriosam natus odio, reiciendis voluptatem!`,
          img:"https://images.unsplash.com/photo-1498837167922-ddd27525d352?ixid=MXwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=1050&q=80",
          chef:"James Hetfield"

        },
        {
          id: 3, name: 'Some food 3',
          textDescription: `Lorem ipsum dolor sit amet, consectetur adipisicing elit. In optio recusandae veritatis. Aliquam asperiores consequatur laboriosam natus odio, reiciendis voluptatem!`,
          img: "https://images.pexels.com/photos/1082343/pexels-photo-1082343.jpeg?auto=compress&cs=tinysrgb&dpr=2&h=650&w=940",
          chef:"Kurt Cobain"

        },
        {
          id: 4, name: 'Some food 4',
          textDescription: `Lorem ipsum dolor sit amet, consectetur adipisicing elit. In optio recusandae veritatis. Aliquam asperiores consequatur laboriosam natus odio, reiciendis voluptatem!`,
          img:"https://images.pexels.com/photos/1527602/pexels-photo-1527602.jpeg?auto=compress&cs=tinysrgb&dpr=2&h=650&w=940",
          chef:"Keith Flint"

        },

      ]
    }
  }
}
</script>
<style>
img {
  cursor: pointer;
}
#foodItems {
  display: flex;
  flex-direction: row;
}
@media (max-width: 1200px) {
  #foodItems {
    flex-direction: column;
  }
}
@media (max-width: 800px) {
  #foodItems {
    flex-direction: column;
  }
}
</style>
