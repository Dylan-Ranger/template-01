<template>
  <ion-page class="ion-padding">
    <PayCardOverview />
    <PeopleComponent :data="people" />
    <FormComponent />
    <ion-button color="dark">
      Send
    </ion-button>
  </ion-page>
</template>

<script>
import { IonPage, IonButton } from "@ionic/vue";

import FormComponent from "@/components/FormComponent.vue";
import PeopleComponent from "@/components/People.vue";
import PayCardOverview from "@/components/PayCardOverview.vue";

export default {
  name: "payPage",
  title: "Pay",
  requiresAuth: false,
  components: {
    IonPage,
    FormComponent,
    PeopleComponent,
    PayCardOverview,
    IonButton
  },
  data() {
    return {
      cards: [
        {
          cardNumber: "4524 3428 898 239",
          balance: "12 354.05",
          accountName: "Savings",
          expDate: "02/2020",
        },
        {
          cardNumber: "9483 2394 8987 8391",
          balance: "1435.20",
          accountName: "Savings",
          expDate: "06/2024",
        },
        {
          cardNumber: "3079 485 2395 3944",
          balance: "8 200",
          accountName: "Savings",
          expDate: "08/2022",
        },
      ],
      people: [
        {
          name: "Person Name",
          image: "assets/img/makazoli.png"
        },
        {
          name: "Person Name",
          image: "assets/img/max.png"
        },
        {
          name: "Person Name",
          image: "assets/img/lewis.png"
        },
        {
          name: "Person Name",
          image: "assets/img/snoop.png"
        }
      ]
    };
  },
  methods: {},
};
</script>

<style lang="scss" scoped>
@media screen and (max-width: 480px) {
  .test{
    display: none;
  }
}

ion-button {
  width: 100%;
  --border-radius: 20px;
  height: 46px;
  text-transform: none;
}
</style>
