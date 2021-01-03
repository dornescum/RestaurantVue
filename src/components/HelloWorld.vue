<template>
  <div>
    <b-card
        overlay
        img-src="https://images.unsplash.com/photo-1428515613728-6b4607e44363?ixid=MXwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=1050&q=80"
        img-alt="Card Image"
        text-variant="white"
        title="Some picture"
        sub-title="Subtitle"
    >
      <b-card-text>
        Some quick example text to build on the card and make up the bulk of the card's content Lorem ipsum dolor sit amet, consectetur adipisicing elit. Aliquam assumenda commodi doloribus illo laudantium magnam magni quos sequi tempore unde.
      </b-card-text>
    </b-card>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
@media (max-width: 600px){
  .card-text {
    font-size: 14px;
  }
}
@media (max-width: 400px){
  .card-text {
    font-size: 12px;
  }
}
</style>
