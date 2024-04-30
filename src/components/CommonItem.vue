<template>
    <ion-item>
      <ion-label>
        <p>Nombre: {{ item.nombre }}</p>
        <p>Descripción: {{ item.descripción }}</p>
      </ion-label>
      <ion-note slot="start">Código: {{ item.código }}</ion-note>
      <ion-note slot="end">Estado: {{ item.estado }}</ion-note>
    </ion-item>
  </template>
  
  <script>
  export default {
    props: {
      item: {
        type: Object,
        required: true
      }
    }
  }
  </script>
  