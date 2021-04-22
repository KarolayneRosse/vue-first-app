<template>
  <base-layout title="All the memories" >
    <ion-list>
      <ion-item @click="() => router.push('/memories/1')">A trip into the mountains</ion-item>
      <ion-item>Surfing the sea side</ion-item>
      <ion-item>Reading a good book</ion-item>
      <ion-item>Good eating</ion-item>
    </ion-list>
  </base-layout>
</template>
<script>
import {
  IonList,
  IonItem,
} from "@ionic/vue";

export default {
  components: [
    IonList,
    IonItem,
  ],
};
</script>
