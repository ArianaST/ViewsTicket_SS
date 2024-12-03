<template>
  <div class="col-span-12 mt-8">
    <div class="intro-y flex items-center h-10">
      <h2 class="text-2xl text-success font-medium leading-none mt-3">INTERNAL MIS TICKETS</h2>
    </div>

    <div class="intro-y box p-5 mt-5">
      <div class="flex flex-col sm:flex-row sm:items-end xl:items-start">
        <form id="tabulator-html-filter-form" class="xl:flex sm:mr-auto">
          <div class="sm:flex items-center sm:mr-4">
            <label class="w-12 flex-none xl:w-auto xl:flex-initial mr-2">Estatus</label>

            <select id="tabulator-html-filter-field" v-model="filter.Estatus"
              class="form-select w-full sm:w-32 2xl:w-full mt-2 sm:mt-0 ">
              <option value="completed">Completo</option>
              <option value="in progress">En progreso</option>
              <option value="cancel">Cancelado</option>
              <option value="nuevo">Nuevo</option>
              <option value="recibido">Recibido</option>
              <option value="rechazado">Rechazado</option>
            </select>
          </div>
          <div class="sm:flex items-center sm:mr-4 mt-2 xl:mt-0">
            <label class="w-12 flex-none xl:w-auto xl:flex-initial mr-2">Prioridad</label>
            <select id="tabulator-html-filter-type" v-model="filter.prioridad"
              class="form-select w-full mt-2 sm:mt-0 sm:w-auto">
              <option value="name">Prioridad</option>
              <option value="alta" selected>Alta</option>
              <option value="media">Media</option>
              <option value="baja">Baja</option>

            </select>
          </div>
          <div class="sm:flex items-center sm:mr-4 mt-2 xl:mt-0">
            <label class="w-12 flex-none xl:w-auto xl:flex-initial mr-2">Buscar</label>
            <input id="tabulator-html-filter-value" v-model="filter.value" type="text"
              class="form-control sm:w-40 2xl:w-full mt-2 sm:mt-0" placeholder="Search..." />
          </div>
          <div class="mt-7 xl:mt-0">
            <button id="tabulator-html-filter-go" type="button" class="btn btn-primary w-full sm:w-16 " @click="onFilter">
              Buscar
            </button>
            <button id="tabulator-html-filter-reset" type="button"
              class="btn btn-secondary w-full sm:w-16 mt-2 sm:mt-0 sm:ml-4" @click="onResetFilter">
              Eliminar
            </button>
          </div>
        </form>
        <div class="flex mt-5 sm:mt-0">
          <button id="tabulator-print" class="btn btn-outline-secondary w-1/2 sm:w-auto mr-2" @click="onPrint">
            <PrinterIcon class="w-4 h-4 mr-2" /> Print
          </button>


        </div>
      </div>


      <!-- END: HTML Table Data -->

      <div class="overflow-x-auto scrollbar-hidden rounded">
        <table class="table mt-5 table-hover rounded-sm">
          <thead class="table-dark rounded-sm">
            <tr>
              <th class="id">ID</th>
              <th class="whitespace-nowrap ">Problema</th>
              <th class="Estatus">Estatus</th>
              <th class="whitespace-nowrap">Descripción</th>
              <th class="Prioridad">Prioridad</th>
              <th class="whitespace-nowrap">Fecha</th>
              <th class="whitespace-nowrap">Solicitante</th>
            </tr>
          </thead>
          <tbody>
            <tr>
              <td value="id">1</td>
              <td> Carga de facturas</td>
              <td>
                <select id="tabulator-html-filter-field" class="form-select w-full sm:w-32 2xl:w-full mt-2 sm:mt-0 ">
                  <option value="Estatus">Estatus</option>
                  <option value="completed">Completo</option>
                  <option value="in progress">En progreso</option>
                  <option value="cancel">Cancelado</option>
                  <option value="new">Nuevo</option>
                  <option value="remaining_stock">Recibido</option>
                  <option value="remaining_stock">Rechazado</option>
                </select>
              </td>
              <td id="Problema">Fallo en el ID de facturas</td>
              <td>
                <select id="tabulator-html-filter-field" class="form-select w-full sm:w-32 2xl:w-full mt-2 sm:mt-0 ">
                  <option value="name">Prioridad</option>
                  <option value="name">Alta</option>
                  <option value="category">Baja</option>
                  <option value="remaining_stock">Media</option>

                </select>
              </td>
              <td> 26/11/2022</td>
              <td> Joel Perez Castillo</td>
            </tr>
            <tr>
              <td id="id">2</td>
              <td id="Problema"> Modificar mensaje de retroalimentacion</td>
              <td>
                <select id="tabulator-html-filter-field" class="form-select w-full sm:w-32 2xl:w-full mt-2 sm:mt-0">
                  <option value="Estatus">Estatus</option>
                  <option value="name">Completo</option>
                  <option value="category">En progreso</option>
                  <option value="remaining_stock">Cancelado</option>
                  <option value="remaining_stock">Nuevo</option>
                  <option value="remaining_stock">Recibido</option>
                  <option value="remaining_stock">Rechazado</option>
                </select>
              </td>
              <td>Mostrar mensajes de segundo plano mas especificos</td>
              <td> <select id="tabulator-html-filter-field" class="form-select w-full sm:w-32 2xl:w-full mt-2 sm:mt-0">
                  <option value="name">Prioridad</option>
                  <option value="name">Alta</option>
                  <option value="category">Baja</option>
                  <option value="remaining_stock">Media</option>
                </select>
              </td>
              <td> 14/01/2023</td>
              <td> Adbel Hernandez Garcia</td>
            </tr>
            <tr>
              <td>3</td>
              <td> Carga de facturas</td>
              <td>
                <select id="tabulator-html-filter-field" class="form-select w-full sm:w-32 2xl:w-full mt-2 sm:mt-0">
                  <option value="Estatus">Estatus</option>
                  <option value="name">Completo</option>
                  <option value="category">En progreso</option>
                  <option value="remaining_stock">Cancelado</option>
                  <option value="remaining_stock">Nuevo</option>
                  <option value="remaining_stock">Recibido</option>
                  <option value="remaining_stock">Rechazado</option>
                </select>
              </td>
              <td>La pagina de facturas no refresca y no actualiza las facturas emitidas</td>
              <td> <select id="tabulator-html-filter-field" class="form-select w-full sm:w-32 2xl:w-full mt-2 sm:mt-0">
                  <option value="name">Prioridad</option>
                  <option value="name">Alta</option>
                  <option value="category">Baja</option>
                  <option value="remaining_stock">Media</option>
                </select></td>
              <td>23/01/2023</td>
              <td>Justino Bieber</td>
            </tr>
            <tr>
              <td>4</td>
              <td> Carga de boots</td>
              <td> <select id="tabulator-html-filter-field" class="form-select w-full sm:w-32 2xl:w-full mt-2 sm:mt-0">
                  <option value="Estatus">Estatus</option>
                  <option value="name">Completo</option>
                  <option value="category">En progreso</option>
                  <option value="remaining_stock">Cancelado</option>
                  <option value="remaining_stock">Nuevo</option>
                  <option value="remaining_stock">Recibido</option>
                  <option value="remaining_stock">Rechazado</option>
                </select> </td>
              <td> No se refrescan los boots</td>
              <td><select id="tabulator-html-filter-field" class="form-select w-full sm:w-32 2xl:w-full mt-2 sm:mt-0 ">
                  <option value="prioridad"> Prioridad</option>
                  <option value="name">Alta</option>
                  <option value="category">Baja</option>
                  <option value="remaining_stock">Media</option>
                </select></td>
              <td>19/03/2023</td>
              <td> Manuel Contreras</td>
            </tr>
            <tr>
              <td>5</td>
              <td> No se obtienen los reportes desde "descargar de reportes general" </td>
              <td> <select id="tabulator-html-filter-field" class="form-select w-full sm:w-32 2xl:w-full mt-2 sm:mt-0">
                  <option value="Estatus">Estatus</option>
                  <option value="name">Completo</option>
                  <option value="category">En progreso</option>
                  <option value="remaining_stock">Cancelado</option>
                  <option value="remaining_stock">Nuevo</option>
                  <option value="remaining_stock">Recibido</option>
                  <option value="remaining_stock">Rechazado</option>
                </select> </td>
              <td> No cargan los reportes en formato pdf </td>
              <td><select id="tabulator-html-filter-field" class="form-select w-full sm:w-32 2xl:w-full mt-2 sm:mt-0 ">

                  <option value="name">Prioridad</option>
                  <option value="name">Alta</option>
                  <option value="category">Baja</option>
                  <option value="remaining_stock">Media</option>
                </select></td>
              <td>30/04/2023</td>
              <td>Desmond Luquen </td>
            </tr>
            <tr>
              <td>6</td>
              <td> Carga de facturas</td>
              <td> <select id="tabulator-html-filter-field" class="form-select w-full sm:w-32 2xl:w-full mt-2 sm:mt-0 ">
                  <option value="Estatus">Estatus</option>
                  <option value="name">Completo</option>
                  <option value="category">En progreso</option>
                  <option value="remaining_stock">Cancelado</option>
                  <option value="remaining_stock">Nuevo</option>
                  <option value="remaining_stock">Recibido</option>
                  <option value="remaining_stock">Rechazado</option>
                </select> </td>
              <td> El apartado de facturas no cargan adecuadamente</td>
              <td> <select id="tabulator-html-filter-field" class="form-select w-full sm:w-32 2xl:w-full mt-2 sm:mt-0">
                  <option value="name">Prioridad</option>
                  <option value="name">Alta</option>
                  <option value="category">Baja</option>
                  <option value="remaining_stock">Media</option>
                </select></td>
              <td>11/05/2023</td>
              <td>Cesar Marín</td>
            </tr>
          </tbody>
        </table>
        <div id="tabulator" ref="tableRef" class="mt-5 table-report table-report--tabulator">

        </div>
      </div>
    </div>


  </div>
</template>

<script setup>
import { ref, reactive, onMounted } from "vue";
import feather from "feather-icons";
import Tabulator from "tabulator-tables";

const tableRef = ref();
const tabulator = ref();
const filter = reactive({
  Estatus: "Estatus",
  prioridad: "Prioridad",
  value: "",
});


const initTabulator = () => {
  tabulator.value = new Tabulator(tableRef.value, {
    ajaxURL: "https://dummy-data.left4code.com",
    ajaxFiltering: true,
    ajaxSorting: true,
    printAsHtml: true,
    printStyled: true,
    pagination: "remote",
    paginationSize: 1,
    paginationSizeSelector: [5, 10, 15],
    layout: "fitColumns",
    responsiveLayout: "collapse",
    placeholder: "No matching records found",


  });
};

// Redraw table onresize
const reInitOnResizeWindow = () => {
  window.addEventListener("resize", () => {
    tabulator.value.redraw();
    feather.replace({
      "stroke-width": 1.5,
    });
  });
};


const onFilter = () => {
  tabulator.value.setFilter(filter.Estatus, filter.prioridad, filter.value);
};


const onResetFilter = () => {
  filter.Estatus = "Estatus";
  filter.prioridad = "prioridad";
  filter.value = "";
  onFilter();
};



const onPrint = () => {
  tabulator.value.print();
};

onMounted(() => {
  initTabulator();
  reInitOnResizeWindow();
});
</script>
