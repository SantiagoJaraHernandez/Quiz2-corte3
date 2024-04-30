<template>
    <ion-page>
      <ion-header>
        <ion-toolbar>
          <ion-title>{{ pageTitle }}</ion-title>
        </ion-toolbar>
      </ion-header>
      <ion-content>
        <ion-list>
          <common-item v-for="rol in roles" :key="rol.id" :item="rol" />
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
        pageTitle: 'Roles',
        roles: [
          {
            id: 1,
            código: 'ROL001',
            nombre: 'Administrador',
            descripción: 'Rol: con acceso total al sistema',
            estado: 'Activo'
          },
          {
            id: 2,
            código: 'ROL002',
            nombre: 'Usuario Regular',
            descripción: 'Rol: con permisos limitados',
            estado: 'Inactivo'
          }
        ]
      };
    }
  };
  </script>
  