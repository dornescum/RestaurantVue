<template>
  <div id="nav">
    <b-navbar toggleable="lg" type="dark" variant="dark">
      <b-navbar-brand to="/">
        <img src="../../assets/lg2.png" alt="">
      </b-navbar-brand>

      <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>

      <b-collapse id="nav-collapse" is-nav>
        <b-navbar-nav>
          <b-nav-item to="/">Home</b-nav-item>
          <b-nav-item to="/about">Reservation</b-nav-item>
<!--          <b-nav-item href="#" disabled>Disabled</b-nav-item>-->
        </b-navbar-nav>

        <!-- Right aligned nav items -->
        <b-navbar-nav class="ml-auto">
          <b-nav-form>
            <b-form-input size="sm" class="mr-sm-2" placeholder="Search" id="input-search"></b-form-input>
            <b-button size="sm" class="my-2 my-sm-0" type="submit" id="btn-search">Search</b-button>
          </b-nav-form>



          <b-nav-item-dropdown right>
            <!-- Using 'button-content' slot -->
            <template #button-content>
<!--              <em>User</em>-->
<!--              <b-avatar variant="primary" text="BV"></b-avatar>-->
              <b-avatar src="https://placekitten.com/300/300"></b-avatar>
            </template>
            <b-dropdown-item href="#">Profile</b-dropdown-item>
            <b-dropdown-item href="#">Sign Out</b-dropdown-item>
          </b-nav-item-dropdown>
        </b-navbar-nav>
      </b-collapse>
    </b-navbar>
  </div>
</template>

<script>
export default {
name: "Navbar"
}
</script>

<style scoped>
img {
  height: 42px;
  width: 120px;
}
@media (max-width: 1200px) {
  img {
    height: 32px;
    width: 65px;
  }
}
@media (max-width: 600px) {
  img {
    height: 42px;
    width: 122px;
    border-radius: var(--radius);
  }
}
.bg-dark {
  background-color: var(--clr-bluePrimary) !important;
}
#nav a {
  font-weight: bold;
  color: var(--clr-grey-1);
}

#nav a.router-link-exact-active {
  color: var(--clr-grey-7);
}

#nav .dropdown-item {
  display: block;
  width: 100%;
  padding: .25rem 1.5rem;
  clear: both;
  font-weight: 400;
  color: #212529;
  text-align: inherit;
  white-space: nowrap;
  background-color: transparent;
  border: 0;
}
@media (max-width: 600px) {
  .form-inline{
    display: flex;
    flex-flow: column;
    /*align-items: center;*/
  }
}


#btn-search{
  background-color: var(--clr-grey-8);
}
#input-search{
width: 50%;
}
</style>