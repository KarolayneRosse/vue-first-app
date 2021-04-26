<template>
  <base-layout title="All the memories">
    <ion-list>
      <ion-item
        v-for="memory in memories"
        :key="memory.id"
        :router-link="`/memories/${memory.id}`"
      >
        <ion-thumbnail slot="start">
          <ion-img
            :src="require(`@/assets/${memory.image}`)"
            :alt="memory.title"
          ></ion-img>
        </ion-thumbnail>
        <ion-label class="ml-2">
          {{ memory.title }}
        </ion-label>
      </ion-item>
    </ion-list>
  </base-layout>
</template>
<script>
import { IonList, IonItem, IonImg, IonThumbnail, IonLabel } from "@ionic/vue";

export default {
  components: {
    IonList,
    IonItem,
    IonImg,
    IonThumbnail,
    IonLabel,
  },
  data() {
    return {
      memories: [
        {
          id: 1,
          image: "mountains.jpg",
          title: "A trip into the mountains",
          description: "It was a really nice trip",
        },
        {
          id: 2,
          image: "surfing.jpg",
          title: "Surfing the sea side",
          description: "The best day",
        },
        {
          id: 3,
          image: "book.jpg",
          title: "Reading a good book",
          description: "Fall in love for this history",
        },
        {
          id: 4,
          image: "really-good-dinner.jpg",
          title: "Good eating",
          description: "It was a really nice dinner",
        },
      ],
    };
  },
};
</script>
