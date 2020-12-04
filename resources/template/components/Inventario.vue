<template>
<div class="container-body">
    <div class="contenedor-tablas">
        <div class="card">
    <div class="card-header border-0">
      <div class="row align-items-center">
        <div class="col">
          <h3 class="mb-0">Inventario</h3>
        </div>
         <!-- Boton lateral -->
        <div class="col text-right">
          <b-button type="primary" size="sm" class="btn_table">Imprimir inventario</b-button>
        </div>
      </div>
    </div>

    <div class="table-responsive">
      <base-table thead-classes="thead-light"
                  :data="tableData">
        <template slot="columns">
          <th>Código</th>
          <th>Descripción</th>
          <th>Fechas extremas</th>
          <th></th>
        </template>

        <template slot-scope="{row}">
          <th scope="row">
            {{row.code}}
          </th>
          <td>
            {{row.description}}
          </td>
          <td>
            {{row.date}}
          </td>
          <td class="text-right">
            <base-dropdown class="dropdown"
                           position="right">
              <a slot="title" class="btn btn-sm btn-icon-only text-light" role="button" data-toggle="dropdown" aria-haspopup="true" aria-expanded="false">
                <i class="ni ni-bullet-list-67"></i>
              </a>

              <template>
                <a class="dropdown-item" href="#">Subir</a>
                <a class="dropdown-item" href="#">Editar</a>
                <a class="dropdown-item" href="#">Eliminar</a>
              </template>
            </base-dropdown>
          </td>
        </template>

      </base-table>
    </div>
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
     name: 'inventario',
     data() {
      return {
        tableData: [
          {
            code: '1025',
            description: 'Documento contrato',
            date: '10/12/2020 hasta 10/1/2021',
            
          },
          {
           code: '1025',
            description: 'Documento contrato',
            date: '10/12/2020 hasta 10/1/2021',
            
          },
          {
            code: '1025',
            description: 'Documento contrato',
            date: '10/12/2020 hasta 10/1/2021',
            
          },
          {
            code: '1025',
            description: 'Documento contrato',
            date: '10/12/2020 hasta 10/1/2021',
            
          },
          {
            code: '1025',
            description: 'Documento contrato',
            date: '10/12/2020 hasta 10/1/2021',
           
          }
        ]
      }
    }
}
</script>
<style scoped>
.btn_table{
  background-color: #8F141B;
  color: #DFD4A6;
  border-radius: 50px;
}
</style>