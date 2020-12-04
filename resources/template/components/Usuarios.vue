<template>
  <div class="container-body">
    <div class="contenedor-tablas">
        <!-- Tabla Simple -->
     <!-- <b-table class="tabla" striped hover :items="items"></b-table>-->
     <!-- Tabla Usuarios -->
     <div class="card shadow"
       :class="type === 'dark' ? 'bg-default': ''">
    <div class="card-header border-0"
         :class="type === 'dark' ? 'bg-transparent': ''">
      <div class="row align-items-center">
        <div class="col">
          <h3 class="mb-0" :class="type === 'dark' ? 'text-white': ''">
            {{title}}
          </h3>
        </div>
        <div class="col text-right">
          <base-button type="primary" size="sm" class="btn_table">Crear nuevo usuario</base-button>
        </div>
      </div>
    </div>

    <div class="table-responsive">
      <base-table class="table align-items-center table-flush"
                  :class="type === 'dark' ? 'table-dark': ''"
                  :thead-classes="type === 'dark' ? 'thead-dark': 'thead-light'"
                  tbody-classes="list"
                  :data="tableData">
        <template slot="columns">
          <th>Nombre</th>
          <th>Apellidos</th>
          <th>identificacion</th>
          <th>Rol</th>
          <th></th>
        </template>

        <template slot-scope="{row}">
          <th scope="row">
            <div class="media align-items-center">
              <a href="#" class="avatar rounded-circle mr-3">
                <img alt="Image placeholderss" src="../assets/img/foto.png"><!-- :src="row.img" -->
              </a>
              <div class="media-body">
                <span class="name mb-0 text-sm">{{row.nombre}}</span>
              </div>
            </div>
          </th>
          <!-- Apellidos -->
          <td class="apellidos">
            {{row.apellidos}}
          </td>
          <!-- Identificacion -->
           <td class="identificacion">
            {{row.identificacion}}
          </td>
          <!-- Rol -->
          <td class="rol">
            {{row.rol}}
          </td>
          <!--  
          <td>
            <div class="avatar-group">
              <a href="#" class="avatar avatar-sm rounded-circle" data-toggle="tooltip" data-original-title="Ryan Tompson">
                <img alt="Image placeholder" src="../assets/img/foto.png">
              </a>
              <a href="#" class="avatar avatar-sm rounded-circle" data-toggle="tooltip" data-original-title="Romina Hadid">
                <img alt="Image placeholder" src="../assets/img/foto.png">
              </a>
              <a href="#" class="avatar avatar-sm rounded-circle" data-toggle="tooltip" data-original-title="Alexander Smith">
                <img alt="Image placeholder" src="../assets/img/foto.png">
              </a>
              <a href="#" class="avatar avatar-sm rounded-circle" data-toggle="tooltip" data-original-title="Jessica Doe">
                <img alt="Image placeholder" src="../assets/img/foto.png">
              </a>
            </div>
          </td>-->

          <!-- <td>
            <div class="d-flex align-items-center">
              <span class="completion mr-2">{{row.completion}}%</span>
              <div>
                <base-progress :type="row.statusType"
                               :show-percentage="false"
                               class="pt-0"
                               :value="row.completion"/>
              </div>
            </div>
          </td>-->
            <!-- Boton de opciones -->
          <td class="text-right">
            <base-dropdown class="dropdown"
                           position="right">
              <a slot="title" class="btn btn-sm btn-icon-only text-light" role="button" data-toggle="dropdown" aria-haspopup="true" aria-expanded="false">
                <i class="ni ni-bullet-list-67"></i>
              </a>

              <template>
                <a class="dropdown-item" href="#">Permisos</a>
                <a class="dropdown-item" href="#">Editar</a>
                <a class="dropdown-item" href="#">Desactivar</a>
              </template>
            </base-dropdown>
          </td>

        </template>

      </base-table>
    </div>
    <!-- Numeracion abajo de la tabla  -->
    <div class="card-footer d-flex justify-content-end"
         :class="type === 'dark' ? 'bg-transparent': ''">
      <base-pagination total="30"></base-pagination>
    </div>

  </div>
    </div>
  </div>
</template>
<script>
export default {
  name: "usuarios",
  /*data() {
    return {
      items: [
        {
          nombre: "Jorge Andrés",
          apellidos: "Cutiva Tafur",
          identificacion: 20161145027,
          rol: "Administrador",
        },
        {
          nombre: "Jorge Andrés",
          apellidos: "Cutiva Tafur",
          identificacion: 20161145027,
          rol: "Administrador",
        },
        {
          nombre: "Jorge Andrés",
          apellidos: "Cutiva Tafur",
          identificacion: 20161145027,
          rol: "Administrador",
        },
        {
          nombre: "Jorge Andrés",
          apellidos: "Cutiva Tafur",
          identificacion: 20161145027,
          rol: "Administrador",
        },
      ],
    };
  },*/
  props: {
      type: {
        type: String
      },
      title: String
    },
    data() {
      return {
        tableData: [
          {
            img: '../assets/img/foto.png',
            nombre: 'Jorge Andrés',
            apellidos: 'Cutiva Tafur',
            identificacion: '1075315469',
            rol: 'Admin',
          },
          {
            img: '../assets/img/foto.png',
            nombre: 'Jorge Andrés',
            apellidos: 'Cutiva Tafur',
            identificacion: '1075315469',
            rol: 'Admin',
          },
          {
           img: '../assets/img/foto.png',
            nombre: 'Jorge Andrés',
            apellidos: 'Cutiva Tafur',
            identificacion: '1075315469',
            rol: 'Admin',
          },
          {
            img: '../assets/img/foto.png',
            nombre: 'Jorge Andrés',
            apellidos: 'Cutiva Tafur',
            identificacion: '1075315469',
            rol: 'Admin',
          },
          {
            img: '../assets/img/foto.png',
            nombre: 'Jorge Andrés',
            apellidos: 'Cutiva Tafur',
            identificacion: '1075315469',
            rol: 'Admin',
          }
        ]
      }
    }
};
</script>
<style scoped>
.h1 {
  color: black;
}
.tabla {
background-color: white;
}
.btn_table{
  background-color: #8F141B;
  color: #DFD4A6;
  border-radius: 50px;
}
</style>