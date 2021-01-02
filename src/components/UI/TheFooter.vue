<template>
  <div id="footer">
    <ul>
      <li>
        <div>
          <b-button v-b-modal.modal-1 id="butonModal">Message us</b-button>

          <b-modal id="modal-1" title="Leave us a message">
            <input type="text">
          </b-modal>
        </div>
      </li>
      <!--      <li>-->
      <!--        <a href="#">-->
      <!--          <BIconMailbox></BIconMailbox>-->
      <!--{{message}}-->
      <!--        </a></li>-->
      <li>
        <a href="#">
          <BIconTelephoneFill></BIconTelephoneFill>
          {{ phoneNumber }}
        </a>
      </li>
    </ul>
  </div>
</template>

<script>
import {BIconTelephoneFill} from 'bootstrap-vue'
// import {BootstrapVueIcons} from 'bootstrap-vue';
export default {
  name: "TheFooter",
  components: {
    // BIcon,
    // BIconMailbox,
    BIconTelephoneFill
  },
  data() {
    return {
      phoneNumber: 'Phone',
      message: 'Leave a message'
    }
  }
}
</script>

<style scoped>
#footer {
  background-color: var(--clr-black);
}

#footer ul {
  display: flex;
  justify-content: space-around;
  color: var(--white);
  padding: 10px;
  margin: 0;
}

#footer ul li {
  list-style-type: none;
}

#butonModal {
  padding: 2px;
  border: none;
  border-color: black;
  background-color: #1f1f1f;
}

#butonModal:active {
  box-shadow: none;

  border-color: red;
  background-color: #1f1f1f;
}
input{
  width: 100%;
  height: 5rem;
}
</style>