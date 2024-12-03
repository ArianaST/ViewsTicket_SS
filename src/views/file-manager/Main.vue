<template>
  <h2 class="text-2xl text-emerald-400 font-medium leading-none mt-12">INTERNAL MIS TICKETS</h2>
  <div class="grid grid-cols-12 gap-6 mt-4">
    <div class="col-span-12 lg:col-span-3 2xl:col-span-2">

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
          <div class="sm:flex items-center sm:mr-6 mt-2 xl:mt-0">
            <label class="w-10 flex-none xl:w-auto xl:flex-initial mr-2">Prioridad</label>
            <select id="tabulator-html-filter-type" v-model="filter.prioridad"
              class="form-select w-full mt-2 sm:mt-0 sm:w-auto">
              <option value="alta" selected>Alta</option>
              <option value="media">Media</option>
              <option value="baja">Baja</option>

            </select>
          </div>
          <div class="sm:flex items-center sm:mr-4 mt-0 ">
            <label class="w-12 flex-none xl:w-auto xl:flex-initial mr-2">Buscar</label>
            <input id="tabulator-html-filter-value" v-model="filter.value" type="text"
              class="form-control sm:w-40 2xl:w-full mt-2 sm:mt-0" placeholder="Buscar..." />
          </div>

          <button id="tabulator-html-filter-go" type="button" class="btn bg-sky-800 text-white w-full sm:w-16 "
            @click="onFilter">
            Buscar
          </button>
          <button id="tabulator-html-filter-reset" type="button"
            class="btn bg-emerald-400 text-white w-full sm:w-16 mt-0 sm:mt-0 sm:ml-3" @click="onResetFilter">
            Eliminar
          </button>
        </form>
      </div>

      <!-- END BUTTONS-->
    </div>



    <!-- BEGIN: Inbox Content -->

    <div class="grind scrollbar-hidden col-span-12 lg:col-span-13 mt-0 ">
      <div class=" inbox box bg-white text-black 2xl:col-span-10 lg:col-span-9 mt-0">

        <div class="flex ml-20 text-black mt-0 pt-4  ">
          <div
            class="flex items-center border-t sm:border-0 border-slate-200/60 pt-5 sm:pt-0 mt-1 sm:mt-0 -mx-5 sm:mx-0 px-5 sm:px-0">
            <a href=""
              class="flex w-45 items-center px-3 py-2 mt-2 rounded-md  dark:bg-darkmode-600  font-medium leading-none">
              <PlusIcon class="w-4 h-4 mr-2 text-emerald-400" /> Tickets nuevos
            </a>

            <a href=""
              class="flex w-45 items-center px-3 py-2 mt-2 rounded-md  dark:bg-darkmode-600  font-medium leading-none">
              <TagIcon class="w-4 h-4 mr-2 text-emerald-400" /> Tickets antiguos
            </a>
            <a href="" class="flex items-center px-3 py-2 mt-2 rounded-md dark:bg-darkmode-900 font-medium leading-none">
              <CheckIcon class="w-4 h-4 mr-2 text-emerald-400" /> Solucionados
            </a>
            <a href="" class="flex items-center px-3 py-2 mt-2 rounded-md dark:bg-darkmode-900 font-medium leading-none">
              <TrashIcon class="w-4 h-4 mr-2 text-emerald-400" /> Eliminados
            </a>
          </div>
        </div>
        

        <div class="p-5 flex bg-flex-col-reverse sm:flex-row text-slate-500 rounded-sm border-b-2 border-emerald-300 border-b-gradient-to-t from-emerald-400 to-sky-900">
    <div class="flex items-center border-t sm:border-0 border-slate-200/60 pt-5 sm:pt-0 mt-1 sm:mt-0 -mx-5 sm:mx-0 px-5 sm:px-0 border-emerald-300" >
            <input class="form-check-input" type="checkbox" />
            <div class="dropdown ml-1 " data-tw-placement="bottom-start">
              <a class="dropdown-toggle w-5 h-5 block text-black" href="javascript:;" aria-expanded="false"
                data-tw-toggle="dropdown">
                <ChevronDownIcon class="w-5 h-5" />
              </a>
              <div class="dropdown-menu w-32">
                <ul class="dropdown-content">
                  <li>
                    <a href="" class="dropdow-item">Todos</a>
                  </li>
                  <li>
                    <a href="" class="dropdown-item">Ningúno</a>
                  </li>
                </ul>
              </div>
            </div>
            <a href="" class="w-5 h-5 ml-5 flex items-center text-black justify-center border-esmerald-400">
              <RefreshCwIcon class="w-4 h-4" />
            </a>
          </div>
        </div>
  




        <!--BEGIN: Table-->

        <div class="text-sky-900 overflow-x-auto border-gradient-to-t from-emerald-400 to-sky-900 rounded">
          <table class="table mt-0 border-emerald-400">
            <thead>
              <tr>
                <th class="whitespace-nowrap border-emerald-300 rounded-sm"></th>
                <th class="whitespace-nowrap border-emerald-300">ID</th>
                <th class="whitespace-nowrap border-emerald-300">PROBLEMA</th>
                <th class="whitespace-nowrap border-emerald-300">ESTATUS</th>
                <th class="whitespace-nowrap border-emerald-300">DESCRIPCIÓN</th>
                <th class="whitespace-nowrap border-emerald-300">PRIORIDAD</th>
                <th class="whitespace-nowrap border-emerald-300">FECHA</th>
                <th class="whitespace-nowrap border-emerald-300">SOLICITANTE</th>
                <th class="whitespace-nowrap border-emerald-300 rounded-sm"></th>
              </tr>
            </thead>
            <!--COLUMNAS-->
            <tbody>

              <tr class="text-black intro-x w-80 border-emerald-300">
                <td class="border-emerald-200">
                  <input class="form-check-input" type="checkbox" />
                </td>
                <td value="id" class="border-emerald-200"> 1</td>
                <td class="border-emerald-200"> Carga de facturas</td>
                <td class="border-emerald-200">
                  <select id="tabulator-html-filter-field"
                    class="form-select text-black w-full sm:w-32 2xl:w-full mt-2 sm:mt-0 ">
                    <option value="Estatus" class="border-emerald-200">Estatus</option>
                    <option value="completed border-emerald-200">Completo</option>
                    <option value="in progress border-emerald-200">En progreso</option>
                    <option value="bg-danger cancel border-emerald-200">Cancelado</option>
                    <option value="new border-emerald-200">Nuevo</option>
                    <option value="remaining_stock border-emerald-200">Recibido</option>
                    <option value="remaining_stock border-emerald-200">Rechazado</option>
                  </select>
                </td>
                <td id="Problema">Fallo en el ID de facturas</td>
                <td>
                  <select id="tabulator-html-filter-field"
                    class="form-select text-black w-full sm:w-32 2xl:w-full mt-2 sm:mt-0 ">
                    <option value="name">Prioridad</option>
                    <option value="name">Alta</option>
                    <option value="category">Baja</option>
                    <option value="remaining_stock">Media</option>

                  </select>
                </td>
                <td> 26/11/2022</td>
                <td> Joel Perez Castillo</td>
                <td>
                  <div class="flex items-center mt-2 ">
                    <button href="javascript:;" data-tw-toggle="modal" data-tw-target="#completo" data-tw-dismiss="modal"
                      class="btn btn-success">
                      <CheckCircleIcon class="w-4 h-4" />
                    </button>
                    <button href="javascript:;" data-tw-toggle="modal" data-tw-target="#eliminar" data-tw-dismiss="modal"
                      class="btn btn-danger ml-3">
                      <TrashIcon class="w-4 h-4" />
                    </button>
                  </div>
                </td>
              </tr>
              <tr class="text-black intro-x w-80 border-emerald-400">
                <td>
                  <input class="form-check-input flex-none" type="checkbox" />
                </td>
                <td id="id"> 2</td>
                <td id="Problema"> Modificar mensaje de retroalimentacion</td>
                <td>
                  <select id="tabulator-html-filter-field"
                    class="form-select text-black w-full sm:w-32 2xl:w-full mt-2  sm:mt-0">
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
                <td> <select id="tabulator-html-filter-field"
                    class="form-select text-black w-full sm:w-32 2xl:w-full mt-2 sm:mt-0">
                    <option value="name">Prioridad</option>
                    <option value="name">Alta</option>
                    <option value="category">Baja</option>
                    <option value="remaining_stock">Media</option>
                  </select>
                </td>
                <td> 14/01/2023</td>
                <td> Adbel Hernandez Garcia</td>
                <td>
                  <div class="flex items-center mt-2 ">
                    <button href="javascript:;" data-tw-toggle="modal" data-tw-target="#completo" data-tw-dismiss="modal"
                      class=" btn btn-success ">
                      <CheckCircleIcon class="w-4 h-4" />
                    </button>
                    <button href="javascript:;" data-tw-toggle="modal" data-tw-target="#eliminar" data-tw-dismiss="modal"
                      class=" btn btn-danger ml-3">
                      <TrashIcon class="w-4 h-4" />
                    </button>
                  </div>
                </td>
              </tr>
              <tr class=" text-black intro-x w-80 ">
                <td>
                  <input class="form-check-input flex-none" type="checkbox" />

                </td>
                <td id="id"> 3</td>
                <td> Carga de facturas</td>
                <td>
                  <select id="tabulator-html-filter-field"
                    class="form-select text-black w-full sm:w-32 2xl:w-full mt-2 sm:mt-0">
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
                <td> <select id="tabulator-html-filter-field"
                    class="form-select text-black w-full sm:w-32 2xl:w-full mt-2 sm:mt-0">
                    <option value="name">Prioridad</option>
                    <option value="name">Alta</option>
                    <option value="category">Baja</option>
                    <option value="remaining_stock">Media</option>
                  </select></td>
                <td>23/01/2023</td>
                <td>Justino Bieber</td>
                <td>
                  <div class="flex items-center mt-2 ">
                    <button href="javascript:;" data-tw-toggle="modal" data-tw-target="#completo" data-tw-dismiss="modal"
                      class=" btn btn-success ">
                      <CheckCircleIcon class="w-4 h-4" />
                    </button>
                    <button href="javascript:;" data-tw-toggle="modal" data-tw-target="#eliminar" data-tw-dismiss="modal"
                      class=" btn btn-danger ml-3">
                      <TrashIcon class="w-4 h-4" />
                    </button>
                  </div>
                </td>
              </tr>
              <tr class="text-black intro-x w-80 ">
                <td>
                  <input class="form-check-input flex-none" type="checkbox" />
                </td>
                <td>4</td>
                <td> Carga de boots</td>
                <td> <select id="tabulator-html-filter-field"
                    class="form-select text-black w-full sm:w-32 2xl:w-full mt-2 sm:mt-0">
                    <option value="Estatus ">Estatus</option>
                    <option value="bg-success">Completo</option>
                    <option value="bg-pending category">En progreso</option>
                    <option value="bg-danger remaining_stock">Cancelado</option>
                    <option value="remaining_stock">Nuevo</option>
                    <option value="remaining_stock">Recibido</option>
                    <option value="remaining_stock">Rechazado</option>
                  </select> </td>
                <td> No se refrescan los boots</td>
                <td><select id="tabulator-html-filter-field"
                    class="form-select text-black w-full sm:w-32 2xl:w-full mt-2 sm:mt-0 ">
                    <option value="prioridad"> Prioridad</option>
                    <option value="name">Alta</option>
                    <option value="category">Baja</option>
                    <option value="remaining_stock">Media</option>
                  </select></td>
                <td>19/03/2023</td>
                <td> Manuel Contreras</td>
                <td>
                  <div class="flex items-center mt-2 ">
                    <button href="javascript:;" data-tw-toggle="modal" data-tw-target="#completo" data-tw-dismiss="modal"
                      class=" btn btn-success ">
                      <CheckCircleIcon class="w-4 h-4" />
                    </button>
                    <button href="javascript:;" data-tw-toggle="modal" data-tw-target="#eliminar" data-tw-dismiss="modal"
                      class=" btn btn-danger ml-3">
                      <TrashIcon class="w-4 h-4" />
                    </button>
                  </div>
                </td>
              </tr>
              <tr class=" text-black intro-x w-80">
                <td>
                  <input class="form-check-input flex-none" type="checkbox" />
                </td>

                <td>5</td>
                <td> No se obtienen los reportes desde "descargar de reportes general" </td>
                <td> <select id="tabulator-html-filter-field"
                    class="form-select text-black w-full sm:w-32 2xl:w-full mt-2 sm:mt-0">
                    <option value="Estatus">Estatus</option>
                    <option value="name">Completo</option>
                    <option value="category">En progreso</option>
                    <option value="remaining_stock">Cancelado</option>
                    <option value="remaining_stock">Nuevo</option>
                    <option value="remaining_stock">Recibido</option>
                    <option value="remaining_stock">Rechazado</option>
                  </select> </td>
                <td> No cargan los reportes en formato pdf </td>
                <td><select id="tabulator-html-filter-field"
                    class="form-select text-black w-full sm:w-32 2xl:w-full mt-2 sm:mt-0 ">

                    <option value="name">Prioridad</option>
                    <option value="name">Alta</option>
                    <option value="category">Baja</option>
                    <option value="remaining_stock">Media</option>
                  </select></td>
                <td>30/04/2023</td>
                <td>Desmond Luquen </td>
                <td>
                  <div class="flex items-center mt-2 ">
                    <button href="javascript:;" data-tw-toggle="modal" data-tw-target="#completo" data-tw-dismiss="modal"
                      class=" btn btn-success ">
                      <CheckCircleIcon class="w-4 h-4" />
                    </button>
                    <button href="javascript:;" data-tw-toggle="modal" data-tw-target="#eliminar" data-tw-dismiss="modal"
                      class=" btn btn-danger ml-3">
                      <TrashIcon class="w-4 h-4" />
                    </button>
                  </div>
                </td>
              </tr>
              <tr class=" text-black intro-x w-80 ">
                <td>
                  <input class="form-check-input flex-none" type="checkbox" />
                </td>
                <td>6</td>
                <td> Carga de facturas</td>
                <td> <select id="tabulator-html-filter-field"
                    class="form-select text-black w-full sm:w-32 2xl:w-full mt-2 sm:mt-0 ">
                    <option value="Estatus">Estatus</option>
                    <option value="name">Completo</option>
                    <option value="category">En progreso</option>
                    <option value="remaining_stock">Cancelado</option>
                    <option value="remaining_stock">Nuevo</option>
                    <option value="remaining_stock">Recibido</option>
                    <option value="remaining_stock">Rechazado</option>
                  </select> </td>
                <td> El apartado de facturas no cargan adecuadamente</td>
                <td> <select id="tabulator-html-filter-field"
                    class="form-select text-black w-full sm:w-32 2xl:w-full mt-2 sm:mt-0">
                    <option value="name">Prioridad</option>
                    <option value="name">Alta</option>
                    <option value="category">Baja</option>
                    <option value="remaining_stock">Media</option>
                  </select></td>
                <td>11/05/2023</td>
                <td>Cesar Marín</td>
                <td>
                  <div class="flex items-center mt-2 ">
                    <button href="javascript:;" data-tw-toggle="modal" data-tw-target="#completo" data-tw-dismiss="modal"
                      class=" btn btn-success ">
                      <CheckCircleIcon class="w-4 h-4" />
                    </button>

                    <button href="javascript:;" data-tw-toggle="modal" data-tw-target="#eliminar" data-tw-dismiss="modal"
                      class=" btn btn-danger ml-3">
                      <TrashIcon class="w-4 h-4" />
                    </button>
                  </div>
                </td>
              </tr>

            </tbody>
          </table>
        </div>


        <div class="p-5 rounded-sm  text-white flex flex-col sm:flex-row items-center text-center sm:text-left ">
          <div class="intro-y text-white col-span-12 flex flex-wrap sm:flex-row sm:flex-nowrap items-center">
            <nav class="w-full text-white sm:w-auto sm:mr-auto">
              <ul class="pagination">
                <li class="page-item text-black">
                  <a class="page-link" href="#">
                    <ChevronsLeftIcon class="w-4 h-4 text-black" />
                  </a>
                </li>
                <li class="page-item">
                  <a class="page-link " href="#">
                    <ChevronLeftIcon class="w-4 h-4 text-black" />
                  </a>
                </li>
                <li class="page-item">
                  <a class="text-center text-black m-3" href="#">...</a>
                </li>
                <li class="page-item">
                  <a class="text-center text-black m-3" href="#">1</a>
                </li>
                <li class="page-item">
                  <a class="text-center text-black m-3" href="#">2</a>
                </li>
                <li class="page-item">
                  <a class="text-black m-3" href="#">3</a>
                </li>
                <li class="page-item">
                  <a class=" text-black m-3" href="#">...</a>
                </li>
                <li class="page-item">
                  <a class="page-link" href="#">
                    <ChevronRightIcon class="w-4 h-4 text-black" />
                  </a>
                </li>
                <li class="page-item">
                  <a class="page-link " href="#">
                    <ChevronsRightIcon class="w-4 h-4 text-black" />
                  </a>
                </li>
              </ul>
            </nav>
            <div id="completo" class="modal" tabindex="-1" aria-hidden="true">
              <div class="modal-dialog">
                <div class="modal-content">
                  <div class="modal-body p-0">
                    <div class="p-5 text-center">
                      <CheckCircleIcon class="w-16 h-16 text-success mx-auto mt-3" />
                      <div class="text-3xl mt-5">Ticket actualizado </div>
                      <div class="text-slate-500 mt-2">Presiona el boton para ver actualización</div>
                    </div>
                    <div class="px-5 pb-8 text-center">
                      <button type="button" data-tw-dismiss="modal" class="btn btn-primary w-24">Ok</button>
                    </div>
                  </div>
                </div>
              </div>
            </div>
          </div>

          <!-- MODALES-->

          <div id="eliminar" data-tw-backdrop="static" class="modal" tabindex="-1" aria-hidden="true">
            <div class="modal-dialog">
              <div class="modal-content">
                <div class="modal-body p-0">
                  <div class="p-5 text-center">
                    <XCircleIcon class="w-16 h-16 text-warning mx-auto mt-3" />
                    <div class="text-3xl mt-5"></div>
                    <div class="text-lg font-medium leading-none mt-3">¿Estas seguro de eliminar este ticket?</div>
                  </div>
                  <div class="modal-footer text-right">
                    <button type="button" data-tw-dismiss="modal" class="btn btn-danger shadow-md w-24 mr-1">Sí</button>
                    <button type="button" data-tw-dismiss="modal" class="btn btn-primary shadow-md w-24 mr-1">No</button>
                  </div>
                </div>
              </div>
            </div>
          </div>
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
