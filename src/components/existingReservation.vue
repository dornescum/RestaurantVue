<template>
  <section>
    <div class="border table-responsive-sm">
      <h5>{{name}}</h5>
      <p>Hour of the reservation is : {{ hour}}</p>
      <p>Number of persons is: {{howMany}}</p>
      <p v-bind:class="classObject"> Any known allergies {{illnes}}</p>
      <p> {{phoneNumber}}</p>
      <p> {{emailAdress}}</p>
    </div>

  </section>
</template>

<script>
export default {
  name: "existingreservation",
  props: ['name', "hour", 'howMany', 'illnes', 'phoneNumber', 'emailAdress'],
  data() {
    return {
      classObject: {
        active: true,
        'text-danger': true,
      },
      // enteredReservation:
      //   {
      //     name: 'Popescu',
      //     hour: "12.30",
      //     numberPerson: '4',
      //     alergies: "none",
      //     id: 1,
      //     phone: '95959'
      //   },
        // {
        //   name: "ionescu",
        //   hour: "19.30",
        //   numberPerson: '2',
        //   alergies: "none",
        //   id: 2
        // }

    }
  },

}
</script>

<style scoped>
.border{
  border-radius: var(--radius);
  padding: 10px;
}
p {
  font-size: 18px;
  font-family: "Indie Flower", cursive;
  font-style: italic;
}
p:hover {
  font-size: 18px;
 color: var(--weird-blue);
}
h5 {
  font-family: "Noto Serif Tamil";
}
</style>