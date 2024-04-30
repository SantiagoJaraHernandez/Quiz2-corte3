<template>
    <ion-page>
      <ion-header>
        <ion-toolbar>
          <ion-title>{{ pageTitle }}</ion-title>
        </ion-toolbar>
      </ion-header>
      <ion-content>
        <ion-list>
          <common-item v-for="modulo in modulos" :key="modulo.id" :item="modulo" />
        </ion-list>
      </ion-content>
    </ion-page>
  </template>
  
  <script>
  import CommonItem from '@/components/CommonItem.vue';
  
  export default {
    components: {
      CommonItem
    },
    data() {
      return {
        pageTitle: 'Módulos',
        modulos: [
          // Lista de módulos con el campo adicional 'ruta'
          {
            id: 1,
            código: 'MOD001',
            nombre: 'Módulo de Usuarios',
            descripción: 'Módulo para gestionar usuarios',
            estado: 'Activo',
            ruta: '/usuarios'
          },
          {
            id: 2,
            código: 'MOD002',
            nombre: 'Módulo de Configuración',
            descripción: 'Módulo para configurar el sistema',
            estado: 'Inactivo',
            ruta: '/configuracion'
          }
        ]
      };
    }
  };
  </script>
  