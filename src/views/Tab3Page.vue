<template>
  <ion-page>
    <ion-header>
      <ion-toolbar>
        <ion-title>Tab 3</ion-title>
      </ion-toolbar>
    </ion-header>
    <ion-content :fullscreen="true">
      <ion-header collapse="condense">
        <ion-toolbar>
          <ion-title size="large">Tab 3</ion-title>
        </ion-toolbar>
      </ion-header>

      <ExploreContainer name="Tab 3 page" />
    </ion-content>
  </ion-page>
</template>

<script lang="ts">
import { defineComponent } from 'vue';
import {
  IonPage, IonHeader, IonToolbar, IonTitle, IonContent,
  onIonViewDidEnter, onIonViewDidLeave, onIonViewWillEnter, onIonViewWillLeave
} from '@ionic/vue';
import ExploreContainer from '@/components/ExploreContainer.vue';

export default defineComponent({
  name: 'Tab3Page',
  components: {
    ExploreContainer,
    IonHeader,
    IonToolbar,
    IonTitle,
    IonContent,
    IonPage
  },
  setup() {
    onIonViewDidEnter(() => {
      console.log('Composition API (lifecycle hooks) page did enter');
    });

    onIonViewDidLeave(() => {
      console.log('Composition API (lifecycle hooks) page did leave');
    });

    onIonViewWillEnter(() => {
      console.log('Composition API (lifecycle hooks) page will enter');
    });

    onIonViewWillLeave(() => {
      console.log('Composition API (lifecycle hooks) page will leave');
    });
  },
});
</script>
