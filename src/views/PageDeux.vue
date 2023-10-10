<template>
    <ion-page>
      <ion-header>
        <ion-toolbar color="primary">
            <ion-buttons slot="start">
                <!-- <ion-back-button @click="this.router.back()"></ion-back-button> -->
                <ion-back-button></ion-back-button>
            </ion-buttons>
          <ion-title>Page 2</ion-title>
        </ion-toolbar>
      </ion-header>
  
      <ion-content>
        <div class="ion-text-center milieu">
            <p>Page 2; Param: {{route.params.id}}</p>
        </div>
      </ion-content>
  
      <ion-footer>
        <ion-toolbar color="secondary">
          <ion-title>Pied de page</ion-title>
        </ion-toolbar>
      </ion-footer>
    </ion-page>
  </template>
  
  <script lang="ts">
  import {
    IonContent,
    IonHeader,
    IonPage,
    IonTitle,
    IonToolbar,
    IonFooter,
    IonButtons,
    IonBackButton,
  } from '@ionic/vue';
  import { defineComponent } from 'vue';
  import { useRoute, useRouter } from 'vue-router';
  
  export default defineComponent({
    components: {
      IonContent,
      IonHeader,
      IonPage,
      IonTitle,
      IonToolbar,
      IonFooter,
    },
    setup() {
        const route = useRoute();
        const router = useRouter();
        return { route, router };
     },
  });
  </script>
  
  <style scoped>
  .milieu {
    height: 100%;
    display: flex;
    justify-content: center;
    align-items: center;
  }
  </style>
  