<template>
  <section id="user-goals">
    <h2 class="pb-2">Make a Reservation</h2>
    <div class="mb-1">

      <input type="number" v-model="howManyPersons" placeholder="  number of persons" class="mb-1">
     <keep-alive>
      <input type="text" v-model="alergiesNotification" placeholder="  alergies">
     </keep-alive>
    </div>
    <div>
      <input type="number" v-model="inputNumber" placeholder="  enter phone" class="mb-1">
      <input type="text" v-model="enteredGoalValue" class="input-group-lg" placeholder="  enter name">
    </div>
    <button @click="addGoal" class="m-3">Reserved</button>
    <!--    ============================================-->
    <p v-if="goals.length === 0" class="pt-2">No Reservation Yet!!</p>
    <ul v-else>
      <li v-for="goal in goals" :key="goal.id" @click="removeGoal">{{ goal }}</li>
    </ul>
    <div>
      <h3>Rezervation for the date {{ date }}</h3>
    </div>
    <h6 class="font-weight-bold">Existing Reservation</h6>

    <existing-reservation v-for="rez in enteredReservation" :key="rez.id"
                          :name="rez.name"
                          :hour="rez.hour"
                          :how-many="rez.numberPerson"
                          id="2"
                          :illnes="rez.alergies"
                          :phone="rez.phone"
                          :email-adress="rez.email"
                          :class="classObject"
    ></existing-reservation>
    <review-custumers></review-custumers>


  </section>

</template>

<script>
import existingReservation from "@/components/existingReservation";
import reviewCustumers from "@/components/reviewCustumers";

export default {
  name: "aboutReservation",
  components: {
    existingReservation,
    reviewCustumers
  },
  data() {
    return {
      enteredGoalValue: '',
      goals: [],
      inputNumber: '',
      howManyPersons: '',
      alergiesNotification: '',
      alert: 'no input',
      date: new Date().toISOString().slice(0, 10),
      enteredReservation: [
        {
          name: 'Popescu A.',
          hour: "12.30",
          numberPerson: '4',
          alergies: "none",
          id: 1,
          phone: '543534534',
          email: 'dsadasd@dsasad.com'
        },
        {
          name: "Ionescu M.",
          hour: "19.30",
          numberPerson: '2',
          alergies: "none",
          id: 2,
          phone: '543534534',
          email: 'dsadasd@dsasad.com'
        },
        {
          name: "Gheorghe I.",
          hour: "19.30",
          numberPerson: '2',
          alergies: "none",
          id: 223,
          phone: '543534534',
          email: 'dsadasd@dsasad.com'
        }
      ],
    }
  },

  methods: {
    addGoal() {
      this.goals.push(this.enteredGoalValue);
      this.enteredGoalValue = '';
      this.goals.push(this.inputNumber)
      this.inputNumber = ''
      this.goals.push(this.howManyPersons)
      this.howManyPersons = ''
      this.goals.push(this.alergiesNotification)
      this.alergiesNotification = ''
      console.log(this.goals)
    },
    removeGoal(index) {
      this.goals.splice(index, 1)
    },
  },
}
</script>

<style scoped>

#user-goals {
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.26);
  margin: 1rem;
  border-radius: 10px;
  padding: 1rem;
  text-align: center;
}

#user-goals h2 {
  font-size: 2rem;
  border-bottom: 4px solid #ccc;
  color: var(--clr-bluePrimary);
  margin: 0 0 1rem 0;
}

#user-goals ul {
  border: 1px solid #dee2e6;
  list-style: none;
  margin: 1rem 0;
  padding: 0;
  border-radius: var(--radius);
}

#user-goals li {
  margin: 16px 0;
  font-size: 18px;
  font-style: italic;
  /*background-color: var(--clr-grey-9);*/
  padding: 0.5rem;
  color: #1f1f1f;
  /*border-radius: var(--transition);*/
}

#user-goals input {
  font: inherit;
  border: 1px solid #ccc;
}

#user-goals input:focus {
  outline: none;
  border-color: #1b995e;
  background-color: #d7fdeb;
}

#user-goals button {
  font: inherit;
  cursor: pointer;
  border: var(--radius) 1px var(--clr-black);
  background-color: var(--clr-bluePrimary);
  color: white;
  padding: 0.05rem 1rem;
  box-shadow: 1px 1px 2px rgba(0, 0, 0, 0.26);
}

#user-goals button:hover,
#user-goals button:active {
  background-color: var(--clr-blueHover);
  border-color: var(--clr-black);
  box-shadow: 1px 1px 4px rgba(0, 0, 0, 0.26);
  border: var(--radius) 1px var(--clr-black);

}


</style>