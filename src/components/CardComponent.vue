<template>
    <ion-card :color="color">
      <ion-card-header>
        <ion-card-title>{{ nombre }}</ion-card-title>
        <ion-card-subtitle>{{ descripcion }}</ion-card-subtitle>
      </ion-card-header>
      <ion-card-content>
        <ion-item>
          <ion-label>ID:</ion-label>
          <ion-text>{{ id }}</ion-text>
        </ion-item>
        <ion-item>
          <ion-label>Código:</ion-label>
          <ion-text>{{ codigo }}</ion-text>
        </ion-item>
        <ion-item>
          <ion-label>Estado:</ion-label>
          <ion-text>{{ estado }}</ion-text>
        </ion-item>
      </ion-card-content>
    </ion-card>
  </template>
  
  <script lang="ts">
  import { IonCard, IonCardHeader, IonCardTitle, IonCardSubtitle, IonCardContent, IonItem, IonLabel, IonText } from '@ionic/vue';
  import { defineComponent } from 'vue';
  
  export default defineComponent({
    components: {
      IonCard,
      IonCardHeader,
      IonCardTitle,
      IonCardSubtitle,
      IonCardContent,
      IonItem,
      IonLabel,
      IonText
    },
    props: {
      id: Number,
      codigo: String,
      nombre: String,
      descripcion: String,
      estado: String,
      color: String
    }
  });
  </script>
  
  <style scoped>
  /* Estilos específicos para el componente */
  </style>
  