<!-- <template>
  <ion-app>
    <ion-router-outlet />
  </ion-app>
</template>

<script setup lang="ts">
import { IonApp, IonRouterOutlet } from '@ionic/vue';
</script> -->

<template>
  <ion-app>
    <ion-split-pane content-id="main-content">
      <ion-menu content-id="main-content" type="overlay">
        <ion-content>
          <ion-list>
            <ion-list-header>Mon menu</ion-list-header>
            <ion-menu-toggle :auto-hide="false">
              <ion-item>
                <ion-icon slot="start" :ios="logoTux" :md="logoTux"></ion-icon>
                <ion-label>Page 1</ion-label>
              </ion-item>
              <ion-item router-link="/PageDeux/1">
                <ion-icon slot="start" :ios="logoTux" :md="logoTux"></ion-icon>
                <ion-label>Page 2</ion-label>
              </ion-item>
            </ion-menu-toggle>
          </ion-list>
        </ion-content>
      </ion-menu>
      <ion-router-outlet id="main-content"></ion-router-outlet>
    </ion-split-pane>
  </ion-app>
</template> 
  
<script lang="ts">

import { IonApp, IonRouterOutlet, IonSplitPane, IonContent, IonList, IonListHeader, IonItem, IonLabel, IonMenu, IonMenuToggle, IonIcon } from '@ionic/vue';
import { defineComponent } from 'vue';
// Importer les icones
import { logoTux } from 'ionicons/icons';

export default defineComponent({
  name: 'App',
  components: {
    IonApp,
    IonRouterOutlet,
    IonSplitPane,
    IonContent,
    IonList,
    IonListHeader,
    IonItem,
    IonLabel,
    IonMenu,
    IonMenuToggle,
    IonIcon
  },
  setup() {
    return {
      logoTux
    }
  }
});
</script>