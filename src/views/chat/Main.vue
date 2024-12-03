<template>
  <div class="col-span-12 mt-8">
    <div class="intro-y flex items-center h-10">
      <h3 class="text-2xl text-emerald-400 font-medium leading-none mt-3">MIS TICKETS</h3>
      <a href="" class="ml-auto flex items-center text-primary">
        <RefreshCcwIcon class="w-4 h-4 mr-3" /> Recargar
      </a>
    </div>
  </div>


  <div class="grid grid-cols-9 gap-6 mt-2 ">
    <div class="col-span-14 sm:col-span-8 xl:col-span-3 intro-y ">
      <div class="report-box zoom-in">
        <div class="box p-5">
          <div class="flex">
            <CheckCircleIcon class="report-box__icon text-success" />
            <div class="ml-auto">
              <Tippy tag="div" class="report-box__indicator bg-success cursor-pointer">
                33%
                <CheckCircleIcon class="w-4 h-4 ml-0.5" />
              </Tippy>
            </div>
          </div>
          <div class="text-3xl font-medium leading-8 mt-6">4</div>
          <div class="text-base text-slate-500 mt-1 ">Tickets completos</div>
        </div>
      </div>
    </div>

    <div class="col-span-12 sm:col-span-8 xl:col-span-3 intro-y">
      <div class="report-box zoom-in">
        <div class="box p-5">
          <div class="flex">
            <XCircleIcon class="report-box__icon text-danger" />
            <div class="ml-auto">
              <Tippy tag="div" class="report-box__indicator bg-danger">
                12%
                <XCircleIcon class="w-4 h-4 ml-0.5" />
              </Tippy>
            </div>
          </div>
          <div class="text-3xl font-medium leading-8 mt-6">0</div>
          <div class="text-base text-slate-500 mt-1">
            Tickets cancelados
          </div>
        </div>
      </div>
    </div>
    <div class="col-span-12 sm:col-span-8 xl:col-span-3 intro-y">
      <div class="report-box zoom-in">
        <div class="box p-5">
          <div class="flex">
            <PlusCircleIcon class="report-box__icon text-primary" />
            <div class="ml-auto">
              <Tippy tag="div" class="report-box__indicator bg-primary">
                22%
                <PlusIcon class="w-4 h-4 ml-0.5" />
              </Tippy>
            </div>
          </div>
          <div class="text-3xl font-medium leading-8 mt-6">0</div>
          <div class="text-base text-slate-500 mt-1">
            Tickets nuevos
          </div>
        </div>
      </div>
    </div>


  </div>
  <br>
  <div class="intro-y chat grid grid-cols-12 gap-5 mt-5">
    <!-- BEGIN: Chat Side Menu -->
    <div class="col-span-12 lg:col-span-4 2xl:col-span-3">
      <div class="intro-y pr-1">
        <div class="box p-2">
          <ul class="nav nav-pills" role="tablist">
            <li id="chats-tab" class="nav-item flex-1" role="presentation">
              <button class="nav-link w-full py-2 active " data-tw-toggle="pill" data-tw-target="#chats" type="button"
                role="tab" aria-controls="chats" aria-selected="true">
                Recientes
              </button>
            </li>
            <li id="friends-tab" class="nav-item flex-1" role="presentation">
              <button class="nav-link w-full py-2" data-tw-toggle="pill" data-tw-target="#friends" type="button"
                role="tab" aria-controls="friends" aria-selected="false">
                Tickets
              </button>
            </li>
          </ul>
        </div>
      </div>
      <div class="tab-content">
        <div id="chats" class="tab-pane active" role="tabpanel" aria-labelledby="chats-tab">

          <div class="chat__chat-list overflow-y-auto scrollbar-hidden pr-0 pt-0 mt-5">
            <div v-for="(faker, fakerKey) in $_.take($f(), 4)" :key="fakerKey"
              class="intro-x cursor-pointer box relative flex items-center p-5" :class="{ 'mt-5': fakerKey }"
              @click="showChatBox">
              <TinySlider ref-key="announcementRef" class="py-1">
                <div class="px-0 text-sky-900">
                  <RefreshCcwIcon class="w-4 h-4 text-primary" />
                  <div class="text-xl font-medium  mt-3"> Actualización</div>
                  <div class="text block font-medium dark:text-slate-500 mt-2">
                    Empresa
                    <div class="text-slate-600 dark:text-slate-500 mt-2"> Descripcion
                    </div>
                  </div>
                  <div class="flex items-center mt-3">
                    <div
                      class="px-9 py-2 bg-dark/10 text-sky-900 dark:bg-darkmode-200 dark:text-slate-300 rounded font-medium mt-4">
                      Hace unos segundos....
                    </div>
                  </div>
                </div>
                <div class="px-0 text-sky-900">
                  <div class="px-0">
                    <SlashIcon class="w-4 h-4" />
                    <div class="text-xl  font-medium leading-none mt-3"> Ticket cancelado</div>
                    <div class="text block font-medium dark:text-slate-500 mt-2">
                      Empresa
                      <div class="text-slate-600 dark:text-slate-500 mt-2"> Descripcion
                      </div>
                    </div>
                    <div class="flex items-center mt-3">
                      <div
                        class="px-9 py-2 bg-dark/10 text-sky-900 dark:bg-darkmode-300 dark:text-slate-300 rounded font-medium mt-4">
                        Hace 2 minutos...

                      </div>
                    </div>
                  </div>
                </div>
                <div class="px-0 text-sky-900">
                  <CheckIcon class="w-4 h-4 text-primary" />
                  <div class="text-xl font-medium  mt-3"> Actualización</div>
                  <div class="text block font-medium dark:text-slate-500 mt-2">
                    Empresa
                    <div class="text-slate-600 dark:text-slate-500 mt-2"> Descripcion
                    </div>
                  </div>
                  <div class="flex items-center mt-3">
                    <div
                      class="px-9 py-2 bg-dark/10 text-sky-900  dark:bg-darkmode-300 dark:text-slate-300 rounded font-medium mt-4">
                      Hace dos semanas...
                    </div>
                  </div>
                </div>
              </TinySlider>
            </div>
          </div>
        </div>
        <div id="friends" class="tab-pane" role="tabpanel" aria-labelledby="friends-tab">
          <br>
          <div class="intro-y col-span-12 lg:col-span-8">
            <div class="lg:flex intro-y">
              <div class="relative">
                <input type="text" class="form-control py-3 px-4 w-full lg:w-35 box pr-0"
                  placeholder="Buscar ticket..." />
                <SearchIcon class="w-4 h-4 absolute my-auto inset-y-0 mr-3 right-0 text-slate-500" />
              </div>
              <select class="form-select py-2 px-2 box w-full lg:w-auto mt-2 lg:mt-0 ml-auto">
                <option>Ordenar</option>
                <option>A a la Z</option>
                <option>Z a la A</option>
                <option>Proximos a vencer</option>
              </select>
            </div>
          </div>

          <div class="chat__user-list overflow-y-auto scrollbar-hidden pr-1 pt-1">
            <div class="mt-4 text-slate-500">Tickets proximos a vencer</div>
            <div class="cursor-pointer box relative flex items-center p-5 mt-5">
              <div class="w-10 h-10 flex-none image-fit mr-1">
                <LayersIcon class="report-box__icon text-primary"></LayersIcon>
                <div class="progress mt-2">
                  <div class="progress-bar w-3/4 bg-warning" role="progressbar" aria-valuenow="0" aria-valuemin="0"
                    aria-valuemax="50"></div>
                </div>
              </div>

              <div class="ml-2 overflow-hidden">
                <div class="flex items-center">
                  <a class="font-medium">Nombre del problema</a>
                </div>
                <div class="w-full truncate text-slate-500 mt-0.5">
                  Descripción
                </div>
              </div>

            </div>
            <div class="cursor-pointer box relative flex items-center p-5 mt-5">
              <div class="w-9 h-9 flex-none image-fit mr-1">
                <LayersIcon class="report-box__icon text-primary" />
                <div class="progress mt-2">
                  <div class="progress-bar w-3/4 bg-warning" role="progressbar" aria-valuenow="0" aria-valuemin="0"
                    aria-valuemax="50"></div>
                </div>
              </div>
              <div class="ml-2 overflow-hidden">
                <div class="flex items-center">
                  <a href="" class="font-medium">Nombre del problema</a>
                </div>
                <div class="w-full truncate text-slate-500 mt-0.5">
                  Descripción
                </div>
              </div>

            </div>
            <div class="mt-4 text-slate-500">Tickets en proceso</div>
            <div class="cursor-pointer box relative flex items-center p-5 mt-5">
              <div class="w-9 h-9 flex-none image-fit mr-1">
                <LayersIcon class="report-box__icon text-primary" />
                <div class="progress mt-3">
                  <div class="progress-bar w-2/3 bg-success" role="progressbar" aria-valuenow="0" aria-valuemin="0"
                    aria-valuemax="100"></div>
                </div>
              </div>
              <div class="ml-2 overflow-hidden">
                <div class="flex items-center">
                  <a class="font-medium"> Nombre del problema</a>
                </div>
                <div class="w-full truncate text-slate-500 mt-0.5">
                  Descripción
                </div>
              </div>

            </div>
            <div class="cursor-pointer box relative flex items-center p-5 mt-5">
              <div class="w-12 h-12 flex-none image-fit mr-1">
                <div class="w-9 h-9 flex-none image-fit mr-1">
                  <LayersIcon class="report-box__icon text-primary" />
                  <div class="progress mt-3">
                    <div class="progress-bar w-2/3 bg-success" role="progressbar" aria-valuenow="0" aria-valuemin="0"
                      aria-valuemax="100"></div>
                  </div>
                </div>
              </div>
              <div class="ml-2 overflow-hidden">
                <div class="flex items-center">
                  <a class="font-medium">Nombre del problema</a>
                </div>
                <div class="w-full truncate text-slate-500 mt-0.5">
                  Descripción
                </div>
              </div>

            </div>
            <div class="cursor-pointer box relative flex items-center p-5 mt-5">
              <div class="w-12 h-12 flex-none image-fit mr-1">
                <div class="w-9 h-9 flex-none image-fit mr-1">
                  <LayersIcon class="report-box__icon text-primary" />
                  <div class="progress mt-3">
                    <div class="progress-bar w-2/3 bg-success" role="progressbar" aria-valuenow="0" aria-valuemin="0"
                      aria-valuemax="100"></div>
                  </div>
                </div>
              </div>
              <div class="ml-2 overflow-hidden">
                <div class="flex items-center">
                  <a class="font-medium">Nombre del problema</a>
                </div>
                <div class="w-full truncate text-slate-500 mt-0.5">
                  Descripción
                </div>
              </div>
            </div>

            <div class="chat__user-list overflow-y-auto scrollbar-hidden pr-1 pt-1">
              <div class="mt-4 text-slate-500">Tickets cancelados</div>
              <div class="cursor-pointer box relative flex items-center p-5 mt-5">
                <div class="w-12 h-12 flex-none image-fit mr-1">
                  <div class="w-9 h-9 flex-none image-fit mr-1">
                    <LayersIcon class="report-box__icon text-primary" />
                    <div class="progress mt-3">
                      <div class="progress-bar w-4/4 bg-danger" role="progressbar" aria-valuenow="0" aria-valuemin="0"
                        aria-valuemax="100"></div>
                    </div>
                  </div>
                </div>
                <div class="ml-2 overflow-hidden">
                  <div class="flex items-center">
                    <a class="font-medium">Nombre del problema</a>
                  </div>
                  <div class="w-full truncate text-slate-500 mt-0.5">
                    Descripción
                  </div>
                </div>
                <div class="dropdown ml-auto">
                  <a class="dropdown-toggle w-5 h-5 block" aria-expanded="false" data-tw-toggle="dropdown"> </a>
                  <div>
                    <button href="javascript:;" data-tw-toggle="modal" data-tw-target="#overlapping-modal-preview20">
                      <Trash2Icon class="w-5 h-5 text-slate-500" />
                    </button>
                  </div>
                  <!-- BEGIN: Modal Toggle -->
                  <div id="overlapping-modal-preview20" class="modal" data-tw-backdrop="static" tabindex="-1"
                    aria-hidden="true">

                    <div class="modal-dialog">
                      <div class="modal-content">
                        <div class="modal-body p-0">
                          <div class="p-5 text-center">
                            <XCircleIcon class="w-16 h-16 text-danger mx-auto mt-3" />
                            <div class="text-3xl mt-5">¿Estas seguro?</div>
                            <div class="text-slate-500 mt-2">
                              ¿Deseas borrar este ticket? <br /> Este proceso no se puede deshacer
                            </div>
                          </div>
                          <div class="px-5 pb-8 text-center">
                            <button type="button" data-tw-dismiss="modal" class="btn btn-outline-secondary w-24 mr-1">
                              Cancel
                            </button>
                            <button type="button" class="btn btn-danger w-24">Delete</button>
                          </div>
                        </div>
                      </div>
                    </div>
                  </div>
                  <div class="dropdown-menu w-40">
                  </div>
                </div>
              </div>
            </div>
          </div>

        </div>
        <div id="profile" class="tab-pane" role="tabpanel" aria-labelledby="profile-tab">
        </div>
      </div>
    </div>


    <!-- END: Chat Side Menu -->
    <!-- BEGIN: Chat Content -->

    <div class="intro-y col-span-9 lg:col-span-8 2x1:col-span-15">
      <div class="chat box bg-transparent">

        <!--GRIND1 END-->
        <div class="grid grid-cols-20 gap-35 mt-0">
          <button class="col-span-12 sm:col-span-6 xl:col-span-3 intro-y">
            <a href="javascript:;" data-tw-toggle="modal" data-tw-target="#overlapping-modal-problem">
              <div id="overlapping-modal-problem" class="modal" tabindex="-1" aria-hidden="true">
                <div class="modal-dialog modal-xl">
                  <div class="modal-content">
                    <div class="modal-header">
                      <div class="text-center">
                        <h2 class="font-medium text-base ">Información</h2>
                      </div>
                      <div>
                        <InfoIcon class="w-5 h-5 ml-8 " />
                      </div>

                      <div
                        class="relative before:hidden before:lg:block before:absolute before:w-[60%] before:h-[4px] before:top-0 before:bottom-10 before:mt-4 before:bg-slate-500 before:dark:bg-darkmode-500 flex flex-col lg:flex-row dark:bg-flex-row-400 dark:border-darkmode-700 justify-center px-15 sm:px-20">
                        <div class="intro-x lg:text-center flex items-center lg:block flex-1 z-10 ">

                          <button class="w-10 h-10 rounded-full btn bg-gradient-to-t from-emerald-400 to-sky-900 text-white">1</button>

                          <div class="lg:w-32 font-medium text-base lg:mt-3 ml-3 lg:mx-auto">Nuevo
                          </div>
                        </div>
                        <div class="intro-x lg:text-center flex items-center mt-5 lg:mt-0 lg:block flex-1 z-10">
                          <button class="w-10 h-10 rounded-full btn bg-gradient-to-t from-emerald-400 to-sky-900 text-white ">2</button>
                          <div class="lg:w-32 font-medium text-base lg:mt-3 ml-3 lg:mx-auto">
                            Recibido
                          </div>
                        </div>
                        <div class="intro-x lg:text-center flex items-center mt-5 lg:mt-0 lg:block flex-1 z-10">
                          <button class="w-10 h-10 rounded-full btn bg-gradient-to-t from-emerald-400 to-sky-900 text-white">3</button>
                          <div class="lg:w-32 font-medium text-base lg:mt-3 ml-3 lg:mx-auto">
                            En progreso
                          </div>
                        </div>
                        <div class="intro-x lg:text-center flex items-center mt-5 lg:mt-0 lg:block flex-1 z-10">

                          <button
                            class="w-10 h-10 rounded-full btn text-slate-500 bg-slate-100 dark:bg-darkmode-400 dark:border-darkmode-400">
                            <img src="../assets/images/kuantik.png">
                          </button>
                          <div class="lg:w-32 font-medium fomt-color-white text-base lg:mt-3 ml-3 lg:mx-auto">
                            Completado
                          </div>
                        </div>
                      </div>
                    </div>


                    <div class="modal-body grid grid-cols-12 gap-4 gap-y-3" @submit.prevent="save">
                      <div class="col-span-12 sm:col-span-12">
                        <label for="horizontal-form-1" class="form-label">Problema</label>
                        <input id="horizontal-form-1" type="text" class="form-control"
                          placeholder="Reportes en altas tickets" :value="$f()[0].users[0].$message" disabled />
                      </div>

                      <div class="col-span-12 sm:col-span-12">
                        <label for="validation-form-6" class="form-label w-full flex flex-col sm:flex-row">
                          Descipción
                        </label>
                        <textarea id="validation-form-6" class="form-control" name="comment"
                          placeholder="Descripcion del problema" :value="$f()[0].users[0].$message" disabled></textarea>
                      </div>

                      <div class="col-span-12 sm:col-span-12">
                        <label for="regular-form-3" class="form-label">Nombre del solicitante</label>
                        <input id="regular-form-3" type="text" class="form-control" placeholder="Input text"
                          :value="$f()[0].users[0].name" disabled />
                      </div>
                      <div class="col-span-12 sm:col-span-12">
                        <label for="regular-form-4" class="form-label">Email</label>
                        <input id="regular-form-4" type="text" class="form-control" placeholder="Input text"
                          :value="$f()[0].users[0].email" disabled />
                      </div>
                      <div class="col-span- sm:col-span-12">
                        <label for="regular-form-5" class="form-label">Nombre de la empresa </label>
                        <input id="regular-form-5" type="text" class="form-control"
                          placeholder="Ingresa el nombre de la empresa" :value="$f()[0].users[0].$message" disabled />
                      </div>
                      <div class="col-span-12 sm:col-span-12">
                        <label for="validation-form-4" class="form-label w-full flex flex-col sm:flex-row">
                          RFC
                        </label>
                        <input id="validation-form-4" type="text" name="rfc" class="form-control"
                          placeholder="TAJI090411OJA" :value="$f()[0].users[0].$message" disabled />
                      </div>
                      <div class="modal-footer">
                        <a href="javascript:;" data-tw-toggle="modal" data-tw-target="#next-overlapping-modal-preview2"
                          type="submit" class=" btn btn-danger shadow-md w-30 mr-6 mb-2">
                          <Trash2Icon class="w-4 h-4 mr-2" /> Eliminar
                        </a>
                      </div>
                    </div>
                  </div>
                  <div id="next-overlapping-modal-preview2" data-tw-backdrop="static" class="modal" tabindex="-1"
                    aria-hidden="true">
                    <div class="modal-dialog">
                      <div class="modal-content">
                        <div class="modal-body p-0">
                          <div class="p-5 text-center">
                            <XCircleIcon class="w-16 h-16 text-warning mx-auto mt-3" />
                            <div class="text-3xl mt-5"></div>
                            <div class="text-lg font-medium leading-none mt-3">¿Estas seguro que quieres borrar este
                              ticket?</div>
                          </div>
                          <div class="modal-footer text-right">
                            <button type="button" data-tw-dismiss="modal"
                              class="btn btn-danger shadow-md w-24 mr-1">Sí</button>
                            <button type="button" data-tw-dismiss="modal"
                              class="btn btn-primary shadow-md w-24 mr-1">No</button>
                          </div>
                        </div>
                      </div>
                    </div>
                  </div>
                </div>
              </div>
              <div class="col-span-12 sm:col-span-8 xl:col-span-3 intro-y rounded-full">
                <div class=" zoom-in">
                  <div class="box p-5">
                    <div class="flex">
                      <div class="flex text-slate-500 text-xs">
                        <div class="mr-auto px-2 py-2 text-primary ">06/06/2023</div>
                      </div>
                      <div
                        class="ml-auto font-medium inline-flex bg-success text-white rounded-full px-2 py-1 text-xs 2xl:text-sm 2xl:p-0 2xl:text-success 2xl:bg-transparent 2xl:flex items-center cursor-pointer 2xl:justify-center">
                        <Tippy content="Completado">
                          Completado
                        </Tippy>
                      </div>
                    </div>
                    <div class="text-3xl font-medium leading-8 mt-5">Nombre del problema</div>
                    <div class="text-base text-slate-500 mt-1">Descripción</div>
                    <div clas="w-full flex text-slate-500 text-xs sm:text-sm">
                      <div class="flex items-center px-0 py-1 border-t border-slate-350/60 dark:border-darkmode-400 mt-2">
                        <div class="text-slate-500 text-xs sm:text-sm mt-2"> Empresa:</div>
                        <div class="w-full text-xs text-primary mt-2 ">Creado por: Dilan Martinez</div>
                        <div class=" text-xs text-primary  block mt-0 "> </div>
                      </div>
                    </div>
                  </div>
                </div>
              </div>
            </a>
          </button>
        </div>

        <!--GRIND1 FINISH-->


        <!----GRIND2 END---->
        <div class="grid grid-cols-20 gap-35 mt-8">
          <button class="col-span-12 sm:col-span-6 xl:col-span-3 intro-y">
            <a href="javascript:;" data-tw-toggle="modal" data-tw-target="#overlapping-modal-problem5">
              <div id="overlapping-modal-problem5" class="modal" tabindex="-1" aria-hidden="true">
                <div class="modal-dialog modal-xl">
                  <div class="modal-content">
                    <div class="modal-header">
                      <div class="text-center">
                        <h2 class="font-medium text-base">Información</h2>
                      </div>
                      <div>
                        <InfoIcon class="w-5 h-5 ml-8" />
                      </div>

                      <div
                        class="relative before:hidden before:lg:block before:absolute before:w-[60%] before:h-[4px] before:top-0 before:bottom-10 before:mt-4 before:bg-slate-500 before:dark:bg-darkmode-500 flex flex-col lg:flex-row dark:bg-flex-row-400 dark:border-darkmode-700 justify-center px-15 sm:px-20">
                        <div class="intro-x lg:text-center flex items-center lg:block flex-1 z-10">
                          <button class="w-10 h-10 rounded-full btn bg-gradient-to-t from-emerald-400 to-sky-900 text-white">1</button>
                          <div class="lg:w-32 font-medium text-base lg:mt-3 ml-3 lg:mx-auto">
                            Nuevo
                          </div>
                        </div>
                        <div class="intro-x lg:text-center flex items-center mt-5 lg:mt-0 lg:block flex-1 z-10">
                          <button class="w-10 h-10 rounded-full btn bg-gradient-to-t from-emerald-400 to-sky-900 text-white">2</button>
                          <div class="lg:w-32 font-medium text-base lg:mt-3 ml-3 lg:mx-auto">
                            Recibido
                          </div>
                        </div>
                        <div class="intro-x lg:text-center flex items-center mt-5 lg:mt-0 lg:block flex-1 z-10">
                          <button
                            class="w-10 h-10 rounded-full btn text-slate-500 bg-slate-100 dark:bg-darkmode-400 dark:border-darkmode-400">
                            <img src="../assets/images/kuantik.png">
                          </button>
                          <div class="lg:w-32 font-medium text-base lg:mt-3 ml-3 lg:mx-auto">
                            En progreso
                          </div>
                        </div>
                        <div class="intro-x lg:text-center flex items-center mt-5 lg:mt-0 lg:block flex-1 z-10">
                          <button
                            class="w-10 h-10 rounded-full btn text-slate-500 bg-slate-100 dark:bg-darkmode-400 dark:border-darkmode-400">
                            4
                          </button>
                          <div class="lg:w-32 text-base lg:mt-3 ml-3 lg:mx-auto text-slate-600 dark:text-slate-400">
                            Completado
                          </div>
                        </div>
                      </div>
                    </div>
                    <div class="modal-body grid grid-cols-12 gap-4 gap-y-3" @submit.prevent="save">
                      <div class="col-span-12 sm:col-span-12">
                        <label for="horizontal-form-1" class="form-label">Problema</label>
                        <input id="horizontal-form-1" type="text" class="form-control"
                          placeholder="Reportes en altas tickets" :value="$f()[0].users[0].$message" disabled />
                      </div>

                      <div class="col-span-12 sm:col-span-12">
                        <label for="validation-form-6" class="form-label w-full flex flex-col sm:flex-row">
                          Descipción
                        </label>
                        <textarea id="validation-form-6" class="form-control" name="comment"
                          placeholder="Descripcion del problema" :value="$f()[0].users[0].$message" disabled></textarea>
                      </div>

                      <div class="col-span-12 sm:col-span-12">
                        <label for="regular-form-3" class="form-label">Nombre del solicitante</label>
                        <input id="regular-form-3" type="text" class="form-control" placeholder="Input text"
                          :value="$f()[0].users[0].name" disabled />
                      </div>
                      <div class="col-span-12 sm:col-span-12">
                        <label for="regular-form-4" class="form-label">Email</label>
                        <input id="regular-form-4" type="text" class="form-control" placeholder="Input text"
                          :value="$f()[0].users[0].email" disabled />
                      </div>
                      <div class="col-span-12 sm:col-span-12">
                        <label for="regular-form-5" class="form-label">Nombre de la empresa </label>
                        <input id="regular-form-5" type="text" class="form-control"
                          placeholder="Ingresa el nombre de la empresa" :value="$f()[0].users[0].$message" disabled />
                      </div>
                      <div class="col-span-12 sm:col-span-12">
                        <label for="validation-form-4" class="form-label w-full flex flex-col sm:flex-row">
                          RFC
                        </label>
                        <input id="validation-form-4" type="text" name="rfc" class="form-control"
                          placeholder="TAJI090411OJA" :value="$f()[0].users[0].$message" disabled />
                      </div>

                    </div>
                  </div>

                  <div class="alert alert-danger alert-dismissible show flex items-center mb-2 mt-3" role="alert">
                    <AlertOctagonIcon class="w-6 h-6 mr-2" /> Este ticket se encuentra en progreso no se puede cancelar


                  </div>
                </div>
              </div>
              <div class="col-span-12 sm:col-span-8 xl:col-span-3 intro-y">
                <div class="zoom-in">
                  <div class="box p-5">
                    <div class="flex">
                      <div class="flex text-slate-500 text-xs">
                        <div class="mr-auto px-2 py-2 text-primary ">06/06/2023</div>
                      </div>
                      <div
                        class="ml-auto font-medium inline-flex bg-warning text-white rounded-full px-2 py-1 text-xs 2xl:text-sm 2xl:p-0 2xl:text-success 2xl:bg-transparent 2xl:flex items-center cursor-pointer 2xl:justify-center">
                        <Tippy tag="div" class="report-box__indicator  cursor-pointer" content="En progreso">
                          En progreso
                        </Tippy>
                      </div>
                    </div>
                    <div class="text-3xl font-medium leading-8 mt-6">Nombre del problema</div>
                    <div class="text-base text-slate-500 mt-1">Descripción</div>
                    <div class="flex items-center px-0 py-1 border-t border-slate-350/60 dark:border-darkmode-400 mt-2">
                      <div class="w-full flex text-slate-500 text-xs sm:text-sm">
                        <div class="mt-2"> Empresa: </div>
                        <div class="ml-auto  text-xs text-primary  block mt-2"> Creado por: Manuel Ibañez</div>
                        <a class="ml-auto text-xs text-primary mt-2  block"> Atendido por: </a>
                        <div class="px-1 py-0 text-xs text-primary font-medium mt-2">
                          María Jose
                        </div>
                      </div>
                    </div>
                  </div>
                </div>
              </div>
            </a>
          </button>
        </div>

        <!--GRIND2 FINISH-->


        <!----GRIND3 END-->
        <div class="grid grid-cols-20 gap-35 mt-8">
          <button class="col-span- sm:col-span-6 xl:col-span-3 intro-y">
            <a href="javascript:;" data-tw-toggle="modal" data-tw-target="#overlapping-modal-problem10">
              <div id="overlapping-modal-problem10" class="modal" tabindex="-1" aria-hidden="true">
                <div class="modal-dialog modal-xl">
                  <div class="modal-content">
                    <div class="modal-header">

                      <div class="text-center">
                        <h2 class="font-medium text-base ">Información</h2>
                      </div>
                      <div>
                        <InfoIcon class="w-5 h-5 ml-8" />
                      </div>

                      <div
                        class="relative before:hidden before:lg:block before:absolute before:w-[60%] before:h-[4px] before:top-0 before:bottom-10 before:mt-4 before:bg-slate-500 before:dark:bg-darkmode-500 flex flex-col lg:flex-row dark:bg-flex-row-400 dark:border-darkmode-700 justify-center px-15 sm:px-20">
                        <div class="intro-x lg:text-center flex items-center lg:block flex-1 z-10">
                          <button class="w-10 h-10 rounded-full btn bg-gradient-to-t from-emerald-400 to-sky-900 text-white">1</button>
                          <div class="lg:w-32 font-medium text-base lg:mt-3 ml-3 lg:mx-auto">
                            Nuevo
                          </div>
                        </div>
                        <div class="intro-x lg:text-center flex items-center mt-5 lg:mt-0 lg:block flex-1 z-10">
                          <button class="w-10 h-10 rounded-full btn bg-gradient-to-t from-emerald-400 to-sky-900 text-white">
                            2
                          </button>
                          <div class="lg:w-32 font-medium text-base lg:mt-3 ml-3 lg:mx-auto">
                            Recibido
                          </div>
                        </div>
                        <div class="intro-x lg:text-center flex items-center mt-5 lg:mt-0 lg:block flex-1 z-10">
                          <button class="w-10 h-10 rounded-full btn bg-gradient-to-t from-emerald-400 to-sky-900 text-white">
                            3
                          </button>
                          <div class="lg:w-32 font-medium text-base lg:mt-3 ml-3 lg:mx-auto">
                            En progreso
                          </div>
                        </div>
                        <div class="intro-x lg:text-center flex items-center mt-5 lg:mt-0 lg:block flex-1 z-10">
                          <button
                            class="w-10 h-10 rounded-full btn text-slate-500 bg-slate-100 dark:bg-darkmode-400 dark:border-darkmode-400">
                            <img src="../assets/images/kuantik.png">
                          </button>
                          <div class="lg:w-32 font-medium text-base lg:mt-3 ml-3 lg:mx-auto">
                            Cancelado
                          </div>
                        </div>
                      </div>
                    </div>
                    <div class="modal-body grid grid-cols-12 gap-4 gap-y-3" @submit.prevent="save">
                      <div class="col-span-12 sm:col-span-12">
                        <label for="horizontal-form-1" class="form-label">Problema</label>
                        <input id="horizontal-form-1" type="text" class="form-control"
                          placeholder="Reportes en altas tickets" :value="$f()[0].users[0].$message" disabled />
                      </div>

                      <div class="col-span-12 sm:col-span-12">
                        <label for="validation-form-6" class="form-label w-full flex flex-col sm:flex-row">
                          Descipción
                        </label>
                        <textarea id="validation-form-6" class="form-control" name="comment"
                          placeholder="Descripcion del problema" :value="$f()[0].users[0].$message" disabled></textarea>
                      </div>

                      <div class="col-span-12 sm:col-span-12">
                        <label for="regular-form-3" class="form-label">Nombre del solicitante</label>
                        <input id="regular-form-3" type="text" class="form-control" placeholder="Input text"
                          :value="$f()[0].users[0].name" disabled />
                      </div>
                      <div class="col-span-12 sm:col-span-12">
                        <label for="regular-form-4" class="form-label">Email</label>
                        <input id="regular-form-4" type="text" class="form-control" placeholder="Input text"
                          :value="$f()[0].users[0].email" disabled />
                      </div>
                      <div class="col-span-12 sm:col-span-12">
                        <label for="regular-form-5" class="form-label">Nombre de la empresa </label>
                        <input id="regular-form-5" type="text" class="form-control"
                          placeholder="Ingresa el nombre de la empresa" :value="$f()[0].users[0].$message" disabled />
                      </div>
                      <div class="col-span-12 sm:col-span-12">
                        <label for="validation-form-4" class="form-label w-full flex flex-col sm:flex-row">
                          RFC
                        </label>
                        <input id="validation-form-4" type="text" name="rfc" class="form-control"
                          placeholder="TAJI090411OJA" :value="$f()[0].users[0].$message" disabled />
                      </div>

                    </div>
                  </div>
                  <br>
                  <div class="alert alert-danger alert-dismissible show flex items-center mb-2" role="alert">
                    <AlertOctagonIcon class="w-6 h-6 mr-2" /> Este ticket se encuentra cancelado


                  </div>
                  <div id="next-overlapping-modal-preview6" data-tw-backdrop="static" class="modal" tabindex="-1"
                    aria-hidden="true">
                    <div class="modal-dialog">
                      <div class="modal-content">
                        <div class="modal-body p-0">
                          <div class="p-5 text-center">
                            <XCircleIcon class="w-16 h-16 text-warning mx-auto mt-3" />
                            <div class="text-3xl mt-5"></div>
                            <div class="text-lg font-medium leading-none mt-3">¿Estas seguro que quieres cancelar este
                              ticket?</div>
                          </div>
                          <div class="modal-footer text-right">
                            <button type="button" data-tw-dismiss="modal"
                              class="btn btn-danger shadow-md w-24 mr-1">Sí</button>
                            <button type="button" data-tw-dismiss="modal"
                              class="btn btn-primary shadow-md w-24 mr-1">No</button>
                          </div>
                        </div>
                      </div>
                    </div>
                  </div>
                </div>
              </div>
              <div class="col-span-12 sm:col-span-6 xl:col-span-3 intro-y">
                <div class="zoom-in">
                  <div class="box p-5">
                    <div class="flex">
                      <div class="flex text-slate-500 text-xs">
                        <div class="mr-auto px-2 py-2 text-primary">06/06/2023</div>
                      </div>
                      <div
                        class="ml-auto font-medium inline-flex bg-danger text-white rounded-full px-2 py-1 text-xs 2xl:text-sm 2xl:p-0 2xl:text-success 2xl:bg-transparent 2xl:flex items-center cursor-pointer 2xl:justify-center">
                        <Tippy tag="div" class="report-box__indicator cursor-pointer" content="Cancelado">
                          Cancelado

                        </Tippy>
                      </div>
                    </div>
                    <div class="text-3xl font-medium leading-8 mt-6">Nombre del problema</div>
                    <div class="text-base text-slate-500 mt-1">Descripción</div>
                    <div class="flex items-center px-0 py-1 border-t border-slate-350/60 dark:border-darkmode-400 mt-2">
                      <div class="w-full flex text-slate-500 text-xs sm:text-sm">
                        <div class="mt-2"> Empresa: </div>
                        <div class="ml-auto mt-2 text-xs text-primary  block"> Creado por: Adrian Benitez</div>
                        <a class="ml-auto text-xs text-primary mt-2 block "> Atendido por: </a>
                        <div class="px-1 py-0 text-xs text-primary font-medium mt-2">Justin Martinez
                        </div>
                      </div>
                    </div>
                  </div>
                </div>
              </div>
            </a>
          </button>
        </div>
        <!----GRIND3 FINISH-->


        <!----GRIND4 END-->
        <div class="grid grid-cols-20 gap-35 mt-8">
          <button class="col-span-12 sm:col-span-6 xl:col-span-3 intro-y">
            <a href="javascript:;" data-tw-toggle="modal" data-tw-target="#overlapping-modal-problem7">
              <div id="overlapping-modal-problem7" class="modal" tabindex="-1" aria-hidden="true">
                <div class="modal-dialog modal-xl">
                  <div class="modal-content">
                    <div class="modal-header">

                      <div class="text-center">
                        <h2 class="font-medium text-base ">Información</h2>
                      </div>
                      <div>
                        <InfoIcon class="w-5 h-5 ml-8" />
                      </div>

                      <div
                        class="relative before:hidden before:lg:block before:absolute before:w-[60%] before:h-[4px] before:top-0 before:bottom-10 before:mt-4 before:bg-slate-300 before:dark:bg-darkmode-400 flex flex-col lg:flex-row dark:bg-flex-row-400 dark:border-darkmode-700 justify-center px-15 sm:px-20">

                        <div class="intro-x lg:text-center flex items-center lg:block flex-1 z-10">
                          <button
                            class="w-10 h-10 rounded-full btn text-slate-500 bg-slate-100 dark:bg-darkmode-400 dark:border-darkmode-400">
                            <img src="../assets/images/kuantik.png">
                          </button>
                          <div class="lg:w-32 font-medium text-base lg:mt-3 ml-3 lg:mx-auto">
                            Nuevo
                          </div>
                        </div>
                        <div class="intro-x lg:text-center flex items-center mt-5 lg:mt-0 lg:block flex-1 z-10">
                          <button
                            class="w-10 h-10 rounded-full btn text-slate-500 bg-slate-100 dark:bg-darkmode-400 dark:border-darkmode-400">
                            2
                          </button>
                          <div class="lg:w-32 text-base lg:mt-3 ml-3 lg:mx-auto text-slate-600 dark:text-slate-400">
                            Recibido
                          </div>
                        </div>
                        <div class="intro-x lg:text-center flex items-center mt-5 lg:mt-0 lg:block flex-1 z-10">
                          <button
                            class="w-10 h-10 rounded-full btn text-slate-500 bg-slate-100 dark:bg-darkmode-400 dark:border-darkmode-400">
                            3
                          </button>
                          <div class="lg:w-32 text-base lg:mt-3 ml-3 lg:mx-auto text-slate-600 dark:text-slate-400">
                            En progreso
                          </div>
                        </div>
                        <div class="intro-x lg:text-center flex items-center mt-5 lg:mt-0 lg:block flex-1 z-10">
                          <button
                            class="w-10 h-10 rounded-full btn text-slate-500 bg-slate-100 dark:bg-darkmode-400 dark:border-darkmode-400">
                            4
                          </button>
                          <div class="lg:w-32 text-base lg:mt-3 ml-3 lg:mx-auto text-slate-600 dark:text-slate-400">
                            Completado
                          </div>
                        </div>
                      </div>

                    </div>
                    <div class="modal-body grid grid-cols-12 gap-4 gap-y-3" @submit.prevent="save">
                      <div class="col-span-12 sm:col-span-12">
                        <label for="horizontal-form-1" class="form-label">Problema</label>
                        <input id="horizontal-form-1" type="text" class="form-control"
                          placeholder="Reportes en altas tickets" :value="$f()[0].users[0].$message" disabled />
                      </div>

                      <div class="col-span-12 sm:col-span-12">
                        <label for="validation-form-6" class="form-label w-full flex flex-col sm:flex-row">
                          Descipción
                        </label>
                        <textarea id="validation-form-6" class="form-control" name="comment"
                          placeholder="Descripcion del problema" :value="$f()[0].users[0].$message" disabled></textarea>
                      </div>

                      <div class="col-span-12 sm:col-span-12">
                        <label for="regular-form-3" class="form-label">Nombre del solicitante</label>
                        <input id="regular-form-3" type="text" class="form-control" placeholder="Input text"
                          :value="$f()[0].users[0].name" disabled />
                      </div>
                      <div class="col-span-12 sm:col-span-12">
                        <label for="regular-form-4" class="form-label">Email</label>
                        <input id="regular-form-4" type="text" class="form-control" placeholder="Input text"
                          :value="$f()[0].users[0].email" disabled />
                      </div>
                      <div class="col-span-12 sm:col-span-12">
                        <label for="regular-form-5" class="form-label">Nombre de la empresa </label>
                        <input id="regular-form-5" type="text" class="form-control"
                          placeholder="Ingresa el nombre de la empresa" :value="$f()[0].users[0].$message" disabled />
                      </div>
                      <div class="col-span-12 sm:col-span-12">
                        <label for="validation-form-4" class="form-label w-full flex flex-col sm:flex-row">
                          RFC
                        </label>
                        <input id="validation-form-4" type="text" name="rfc" class="form-control"
                          placeholder="TAJI090411OJA" :value="$f()[0].users[0].$message" disabled />
                      </div>
                      <div class="modal-footer">
                        <a href="javascript:;" data-tw-toggle="modal" data-tw-target="#next-overlapping-modal-preview7"
                          type="submit" class=" btn btn-danger shadow-md w-30 mr-6 mb-2">
                          <SlashIcon class="w-4 h-4 mr-2" /> Cancelar
                        </a>
                      </div>
                    </div>
                  </div>
                  <div id="next-overlapping-modal-preview7" data-tw-backdrop="static" class="modal" tabindex="-1"
                    aria-hidden="true">
                    <div class="modal-dialog">
                      <div class="modal-content">
                        <div class="modal-body p-0">
                          <div class="p-5 text-center">
                            <XCircleIcon class="w-16 h-16 text-warning mx-auto mt-3" />
                            <div class="text-3xl mt-5"></div>
                            <div class="text-lg font-medium leading-none mt-3">¿Estas seguro de cancelar este ticket?
                            </div>
                          </div>
                          <div class="modal-footer text-right">
                            <button type="button" data-tw-dismiss="modal"
                              class="btn btn-danger shadow-md w-24 mr-1">Sí</button>
                            <button type="button" data-tw-dismiss="modal"
                              class="btn btn-primary shadow-md w-24 mr-1">No</button>
                          </div>
                        </div>
                      </div>
                    </div>
                  </div>
                </div>
              </div>

              <div class="col-span-12 sm:col-span-8 xl:col-span-3 intro-y">
                <div class="zoom-in">
                  <div class="box p-5">
                    <div class="flex">
                      <div class="flex text-slate-500 text-xs">
                        <div class="mr-auto px-2 py-2 text-primary">06/06/2023</div>
                      </div>
                      <div
                        class="ml-auto font-medium inline-flex bg-primary text-white rounded-full px-5 py-1 text-xs 2xl:text-sm 2xl:p-0 2xl:text-success 2xl:bg-transparent 2xl:flex items-center cursor-pointer 2xl:justify-center">
                        <Tippy tag="div" class="report-box__indicator cursor-pointer" content="Nuevo">
                          Nuevo

                        </Tippy>
                      </div>
                    </div>
                    <div class="text-3xl font-medium leading-8 mt-6">Nombre del problema</div>
                    <div class="text-base text-slate-500 mt-1">Descripción</div>
                    <div class="flex items-center px-0 py-1 border-t border-slate-350/60 dark:border-darkmode-400 mt-2">
                      <div class="mt-2 text-slate-500 "> Empresa: </div>
                      <div class="ml-auto mt-2 text-xs text-primary  block"> Creado por: Desmond Luqe</div>
                      <a class="ml-auto text-xs text-primary mt-2 block"> Atendido por: </a>
                      <div class="px-1 py-0 text-xs text-primary mt-2 font-medium">
                        Adbel René
                      </div>
                    </div>
                  </div>
                </div>
              </div>
            </a>
          </button>
        </div>

        <!----GRIND4 FINISH-->


        <div class="grid grid-cols-20 gap-35 mt-8">
          <button class="col-span-12 sm:col-span-6 xl:col-span-3 intro-y">
            <a href="javascript:;" data-tw-toggle="modal" data-tw-target="#overlapping-modal-problem11">
              <div id="overlapping-modal-problem11" class="modal" tabindex="-1" aria-hidden="true">
                <div class="modal-dialog modal-xl">
                  <div class="modal-content">
                    <div class="modal-header">
                      <div class="text-center">
                        <h2 class="font-medium text-base ">Información</h2>
                      </div>
                      <div>
                        <InfoIcon class="w-5 h-5 ml-8" />
                      </div>

                      <div
                        class="relative before:hidden before:lg:block before:absolute before:w-[60%] before:h-[4px] before:top-0 before:bottom-10 before:mt-4 before:bg-slate-300 before:dark:bg-darkmode-400 flex flex-col lg:flex-row dark:bg-flex-row-400 dark:border-darkmode-700 justify-center px-15 sm:px-20">
                        <div class="intro-x lg:text-center flex items-center lg:block flex-1 z-10">
                          <button class="w-10 h-10 rounded-full btn bg-gradient-to-t from-emerald-400 to-sky-900 text-white">1</button>
                          <div class="lg:w-32 font-medium text-base lg:mt-3 ml-3 lg:mx-auto">
                            Nuevo
                          </div>
                        </div>
                        <div class="intro-x lg:text-center flex items-center mt-5 lg:mt-0 lg:block flex-1 z-10">
                          <button
                            class="w-10 h-10 rounded-full btn text-slate-500 bg-slate-100 dark:bg-darkmode-400 dark:border-darkmode-400">
                            <img src="../assets/images/kuantik.png">
                          </button>
                          <div class="lg:w-32 font-medium text-base lg:mt-3 ml-3 lg:mx-auto">
                            Recibido
                          </div>
                        </div>
                        <div class="intro-x lg:text-center flex items-center mt-5 lg:mt-0 lg:block flex-1 z-10">
                          <button
                            class="w-10 h-10 rounded-full btn text-slate-500 bg-slate-100 dark:bg-darkmode-400 dark:border-darkmode-400">
                            3
                          </button>
                          <div class="lg:w-32 text-base lg:mt-3 ml-3 lg:mx-auto text-slate-600 dark:text-slate-400">
                            En progreso
                          </div>
                        </div>
                        <div class="intro-x lg:text-center flex items-center mt-5 lg:mt-0 lg:block flex-1 z-10">
                          <button
                            class="w-10 h-10 rounded-full btn text-slate-500 bg-slate-100 dark:bg-darkmode-400 dark:border-darkmode-400">
                            4
                          </button>
                          <div class="lg:w-32 text-base lg:mt-3 ml-3 lg:mx-auto text-slate-600 dark:text-slate-400">
                            Completado
                          </div>
                        </div>
                      </div>

                    </div>
                    <div class="modal-body grid grid-cols-12 gap-4 gap-y-3" @submit.prevent="save">
                      <div class="col-span-12 sm:col-span-12">
                        <label for="horizontal-form-1" class="form-label">Problema</label>
                        <input id="horizontal-form-1" type="text" class="form-control"
                          placeholder="Reportes en altas tickets" :value="$f()[0].users[0].$message" disabled />
                      </div>

                      <div class="col-span-12 sm:col-span-12">
                        <label for="validation-form-6" class="form-label w-full flex flex-col sm:flex-row">
                          Descipción
                        </label>
                        <textarea id="validation-form-6" class="form-control" name="comment"
                          placeholder="Descripcion del problema" :value="$f()[0].users[0].$message" disabled></textarea>
                      </div>

                      <div class="col-span-12 sm:col-span-12">
                        <label for="regular-form-3" class="form-label">Nombre del solicitante</label>
                        <input id="regular-form-3" type="text" class="form-control" placeholder="Input text"
                          :value="$f()[0].users[0].name" disabled />
                      </div>
                      <div class="col-span-12 sm:col-span-12">
                        <label for="regular-form-4" class="form-label">Email</label>
                        <input id="regular-form-4" type="text" class="form-control" placeholder="Input text"
                          :value="$f()[0].users[0].email" disabled />
                      </div>
                      <div class="col-span-12 sm:col-span-12">
                        <label for="regular-form-5" class="form-label">Nombre de la empresa </label>
                        <input id="regular-form-5" type="text" class="form-control"
                          placeholder="Ingresa el nombre de la empresa" :value="$f()[0].users[0].$message" disabled />
                      </div>
                      <div class="col-span-12 sm:col-span-12">
                        <label for="validation-form-4" class="form-label w-full flex flex-col sm:flex-row">
                          RFC
                        </label>
                        <input id="validation-form-4" type="text" name="rfc" class="form-control"
                          placeholder="TAJI090411OJA" :value="$f()[0].users[0].$message" disabled />
                      </div>
                      <div class="modal-footer">
                        <a href="javascript:;" data-tw-toggle="modal" data-tw-target="#next-overlapping-modal-preview11"
                          type="submit" class=" btn btn-danger shadow-md w-30 mr-6 mb-2">
                          <SlashIcon class="w-4 h-4 mr-2" /> Cancelar
                        </a>
                      </div>
                    </div>
                  </div>
                  <div id="next-overlapping-modal-preview11" data-tw-backdrop="static" class="modal" tabindex="-1"
                    aria-hidden="true">
                    <div class="modal-dialog">
                      <div class="modal-content">
                        <div class="modal-body p-0">
                          <div class="p-5 text-center">
                            <XCircleIcon class="w-16 h-16 text-warning mx-auto mt-3" />
                            <div class="text-3xl mt-5"></div>
                            <div class="text-lg font-medium leading-none mt-3">¿Estas seguro de cancelar este ticket?
                            </div>
                          </div>
                          <div class="modal-footer text-right">
                            <button type="button" data-tw-dismiss="modal"
                              class="btn btn-danger shadow-md w-24 mr-1">Sí</button>
                            <button type="button" data-tw-dismiss="modal"
                              class="btn btn-primary shadow-md w-24 mr-1">No</button>
                          </div>
                        </div>
                      </div>
                    </div>
                  </div>
                </div>
              </div>

              <div class="col-span-12 sm:col-span-8 xl:col-span-3 intro-y">
                <div class="zoom-in">
                  <div class="box p-5">
                    <div class="flex">
                      <div class="flex text-slate-500 text-xs">
                        <div class="mr-auto px-2 py-2 text-primary">06/06/2023</div>
                      </div>
                      <div
                        class="ml-auto font-medium inline-flex bg-slate-500  text-white rounded-full px-3 py-1 text-xs 2xl:text-sm 2xl:p-0 2xl:text-success 2xl:bg-transparent 2xl:flex items-center cursor-pointer 2xl:justify-center">
                        <Tippy tag="div" class="report-box__indicator cursor-pointer" content="Recibido">
                          Recibido
                        </Tippy>
                      </div>
                    </div>
                    <div class="text-3xl font-medium leading-8 mt-6">Nombre del problema</div>
                    <div class="text-base text-slate-500 mt-1">Descripción</div>
                    <div class="flex items-center px-0 py-1 border-t border-slate-350/60 dark:border-darkmode-400 mt-2">
                      <div class="w-full flex text-slate-500 text-xs sm:text-sm">
                        <div class="mt-2"> Empresa: </div>
                        <div class="ml-auto mt-2 text-xs text-primary  block"> Creado por: Valeria Gaspar</div>
                        <a class="ml-auto text-xs text-primary mt-2 block"> Atendido por: </a>
                        <div class="px-1 py-0 mt-2 text-xs text-primary font-medium">
                          Victor Chacon
                        </div>
                      </div>
                    </div>
                  </div>
                </div>
              </div>
            </a>
          </button>
        </div>



        <!----GRIND5 END--->


        <div class="grid grid-cols-20 gap-35 mt-8">
          <button class="col-span-12 sm:col-span-6 xl:col-span-3 intro-y">
            <a href="javascript:;" data-tw-toggle="modal" data-tw-target="#overlapping-modal-problem12">
              <div id="overlapping-modal-problem12" class="modal" tabindex="-1" aria-hidden="true">
                <div class="modal-dialog modal-xl">
                  <div class="modal-content">
                    <div class="modal-header">

                      <div class="text-center">
                        <h2 class="font-medium text-base ">Información</h2>
                      </div>
                      <div>
                        <InfoIcon class="w-5 h-5 ml-8" />
                      </div>

                      <div
                        class="relative before:hidden before:lg:block before:absolute before:w-[60%] before:h-[4px] before:top-0 before:bottom-10 before:mt-4 before:bg-slate-500 before:dark:bg-darkmode-500 flex flex-col lg:flex-row dark:bg-flex-row-400 dark:border-darkmode-700 justify-center px-15 sm:px-20">
                        <div class="intro-x lg:text-center flex items-center lg:block flex-1 z-10">
                          <button class="w-10 h-10 rounded-full btn bg-gradient-to-t from-emerald-400 to-sky-900 text-white">1</button>
                          <div class="lg:w-32 font-medium text-base lg:mt-3 ml-3 lg:mx-auto">
                            Nuevo
                          </div>
                        </div>
                        <div class="intro-x lg:text-center flex items-center mt-5 lg:mt-0 lg:block flex-1 z-10">
                          <button class="w-10 h-10 rounded-full btn bg-gradient-to-t from-emerald-400 to-sky-900 text-white">
                            2
                          </button>
                          <div class="lg:w-32 font-medium text-base lg:mt-3 ml-3 lg:mx-auto">
                            Recibido
                          </div>
                        </div>
                        <div class="intro-x lg:text-center flex items-center mt-5 lg:mt-0 lg:block flex-1 z-10">
                          <button class="w-10 h-10 rounded-full btn bg-gradient-to-t from-emerald-400 to-sky-900 text-white">
                            3
                          </button>
                          <div class="lg:w-32 font-medium text-base lg:mt-3 ml-3 lg:mx-auto">
                            En progreso
                          </div>
                        </div>
                        <div class="intro-x lg:text-center flex items-center mt-5 lg:mt-0 lg:block flex-1 z-10">
                          <button
                            class="w-10 h-10 rounded-full btn text-slate-500 bg-slate-100 dark:bg-darkmode-400 dark:border-darkmode-400">
                            <img src="../assets/images/kuantik.png">
                          </button>
                          <div class="lg:w-32 font-medium text-base lg:mt-3 ml-3 lg:mx-auto">
                            Rechazado
                          </div>
                        </div>
                      </div>

                    </div>
                    <div class="modal-body grid grid-cols-12 gap-4 gap-y-3" @submit.prevent="save">
                      <div class="col-span-12 sm:col-span-12">
                        <label for="horizontal-form-1" class="form-label">Problema</label>
                        <input id="horizontal-form-1" type="text" class="form-control"
                          placeholder="Reportes en altas tickets" :value="$f()[0].users[0].$message" disabled />
                      </div>

                      <div class="col-span-12 sm:col-span-12">
                        <label for="validation-form-6" class="form-label w-full flex flex-col sm:flex-row">
                          Descipción
                        </label>
                        <textarea id="validation-form-6" class="form-control" name="comment"
                          placeholder="Descripcion del problema" :value="$f()[0].users[0].$message" disabled></textarea>
                      </div>

                      <div class="col-span-12 sm:col-span-12">
                        <label for="regular-form-3" class="form-label">Nombre del solicitante</label>
                        <input id="regular-form-3" type="text" class="form-control" placeholder="Input text"
                          :value="$f()[0].users[0].name" disabled />

                      </div>
                      <div class="col-span-12 sm:col-span-12">
                        <label for="regular-form-4" class="form-label">Email</label>
                        <input id="regular-form-4" type="text" class="form-control" placeholder="Input text"
                          :value="$f()[0].users[0].email" disabled />
                      </div>
                      <div class="col-span-12 sm:col-span-12">
                        <label for="regular-form-5" class="form-label">Nombre de la empresa </label>
                        <input id="regular-form-5" type="text" class="form-control"
                          placeholder="Ingresa el nombre de la empresa" :value="$f()[0].users[0].$message" disabled />
                      </div>
                      <div class="col-span-12 sm:col-span-12">
                        <label for="validation-form-4" class="form-label w-full flex flex-col sm:flex-row">
                          RFC
                        </label>
                        <input id="validation-form-4" type="text" name="rfc" class="form-control"
                          placeholder="TAJI090411OJA" :value="$f()[0].users[0].$message" disabled />
                      </div>
                      <div class="modal-footer">
                        <a href="javascript:;" data-tw-toggle="modal" data-tw-target="#next-overlapping-modal-preview12"
                          type="submit" class=" btn btn-danger shadow-md w-30 mr-6 mb-2">
                          <Trash2Icon class="w-4 h-4 mr-2" /> Eliminar
                        </a>
                      </div>
                    </div>
                  </div>
                  <div id="next-overlapping-modal-preview12" data-tw-backdrop="static" class="modal" tabindex="-1"
                    aria-hidden="true">
                    <div class="modal-dialog">
                      <div class="modal-content">
                        <div class="modal-body p-0">
                          <div class="p-5 text-center">
                            <XCircleIcon class="w-16 h-16 text-warning mx-auto mt-3" />
                            <div class="text-3xl mt-5"></div>
                            <div class="text-lg font-medium leading-none mt-3">¿Estas seguro de eliminar este ticket?
                            </div>
                          </div>
                          <div class="modal-footer text-right">
                            <button type="button" data-tw-dismiss="modal"
                              class="btn btn-danger shadow-md w-24 mr-1">Sí</button>
                            <button type="button" data-tw-dismiss="modal"
                              class="btn btn-primary shadow-md w-24 mr-1">No</button>
                          </div>
                        </div>
                      </div>
                    </div>
                  </div>
                </div>
              </div>

              <div class="col-span-12 sm:col-span-8 xl:col-span-3 intro-y">
                <div class="zoom-in">
                  <div class="box p-5">
                    <div class="flex">
                      <div class="flex text-slate-500 text-xs">
                        <div class="mr-auto px-2 py-2 text-primary ">06/06/2023</div>
                      </div>
                      <div
                        class="ml-auto font-medium inline-flex bg-pending text-white rounded-full px-2 py-1 text-xs 2xl:text-sm 2xl:p-0 2xl:text-success 2xl:bg-transparent 2xl:flex items-center cursor-pointer 2xl:justify-center">
                        <Tippy tag="div" class="report-box__indicator  cursor-pointer" content="Rechazado">
                          Rechazado

                        </Tippy>
                      </div>
                    </div>
                    <div class="text-3xl font-medium leading-8 mt-6 ">Nombre del problema</div>
                    <div class="text-base text-slate-500 mt-1">Descripción</div>
                    <div class="flex items-center px-0 py-1 border-t border-slate-350/60 dark:border-darkmode-400 mt-2">
                      <div class="w-full flex text-slate-500 text-xs sm:text-sm">
                        <div class="mt-2"> Empresa: </div>
                        <div class="ml-auto mt-2 text-xs text-primary  block"> Creado por: Manuel Ibañez</div>
                        <a class="ml-auto text-xs mt-2 text-primary  block"> Atendido por: </a>
                        <div class="px-1 py-0 text-xs mt-2 text-primary font-medium">
                          Miriam Castillo
                        </div>
                      </div>
                    </div>
                  </div>
                </div>
              </div>
            </a>
          </button>

        </div>

        <!---GRND5 FINISH --->

        <!-- BEGIN: Modal Toggle -->
        <div>
          <a href="javascript:;" data-tw-toggle="modal" data-tw-target="#button-slide-over-preview"
            class="btn btn-rounded-primary bg-sky-900 shadow-md mt-8 ">
            <PlusCircleIcon class="w-9 h-9 " />
          </a>
        </div>
        <!-- BEGIN: Modal Toggle -->
        <div id="button-slide-over-preview" class="modal modal-slide-over" data-tw-backdrop="static" tabindex="-1"
          aria-hidden="true">
          <div class="modal-dialog ">
            <div class="modal-content">
              <div class="intro-y box py-1100 sm:py-100 mt-100">
              </div>

              <!-- END: Modal Header -->
              <div class="modal-header">
                <h2 class="font-medium text-base mr-auto">Levantar ticket</h2>
                <button class="btn btn-outline-secondary hidden sm:flex">
                  <FileIcon class="w-3 h-3 mr-2" /> Download Docs
                  <input type="file" class=" absolute opacity-0" />
                </button>
              </div>
              <div class="modal-body grid grid-cols-12 gap-4 gap-y-3" @submit.prevent="save">
                <div class="col-span-12 sm:col-span-12">
                  <label for="horizontal-form-1" class="form-label">Problema</label>
                  <input id="horizontal-form-1" type="text" class="form-control" placeholder="Ingresa el problema" />
                </div>

                <div class="col-span-12 sm:col-span-12">
                  <label for="validation-form-6" class="form-label w-full flex flex-col sm:flex-row">
                    Descipción
                    <span class="sm:ml-auto mt-1 sm:mt-0 text-xs text-slate-500">
                      al menos 10 caracteres</span>
                  </label>
                  <textarea id="validation-form-6" v-model.trim="validate.comment.$model" class="form-control"
                    :class="{ 'border-danger': validate.comment.$error }" name="comment"
                    placeholder="Escribe la descripcion del problema"></textarea>
                  <template v-if="validate.comment.$error">
                    <div v-for="(error, index) in validate.comment.$errors" :key="index" class="text-danger mt-2">
                      {{ error.$message }}
                    </div>
                  </template>
                </div>
                <div class="col-span-12 sm:col-span-12">
                  <label for="regular-form-3" class="form-label">Nombre del solicitante</label>
                  <input id="regular-form-3" type="text" class="form-control" placeholder="Ej.Abisai Gomez Peralta" />
                </div>
                <div class="col-span-12 sm:col-span-12">
                  <label for="regular-form-4" class="form-label">Email</label>
                  <input id="regular-form-4" type="text" class="form-control" placeholder="example@gmail.com" />
                </div>
                <div class="col-span-12 sm:col-span-12">
                  <label for="regular-form-5" class="form-label">Nombre de la empresa </label>
                  <input id="regular-form-5" type="text" class="form-control"
                    placeholder="Ingresa el nombre de la empresa" />
                </div>
                <div class="col-span-12 sm:col-span-12">
                  <label for="validation-form-4" class="form-label w-full flex flex-col sm:flex-row">
                    RFC
                    <span class="sm:ml-auto mt-1 sm:mt-0 text-xs text-slate-500">Requiere 13 caracteres</span>
                  </label>
                  <input id="validation-form-4" v-model.trim="validate.RFC.$model" type="text" name="rfc"
                    class="form-control" :class="{ 'border-danger': validate.RFC.$error }" placeholder="TAJI090411OJA" />
                  <template v-if="validate.RFC.$error">
                    <div v-for="(error, index) in validate.RFC.$errors" :key="index" class="text-danger mt-2">
                      {{ error.$message }}
                    </div>
                  </template>

                </div>



                <!-- BEGIN: Overlapping Modal Toggle -->
                <div class="modal-footer">
                  <button type="button" href="javascript:;" data-tw-toggle="modal"
                    data-tw-target="#next-overlapping-modal-preview" data-tw-dismiss="modal"
                    class=" flex btn btn-elevated-secondary w-24 mr-5 mb-2">Enviar</button>
                  <button type="button" data-tw-dismiss="modal"
                    class="ml-auto btn btn-elevated-primary w-24 mb-2 mr-2">Cerrar</button>
                </div>
                <!-- END: Overlapping Modal Toggle -->
              </div>
              <!-- BEGIN: Overlapping Modal Content -->
              <div id="next-overlapping-modal-preview" class="modal" tabindex="-1" aria-hidden="true">
                <div class="modal-dialog">
                  <div class="modal-content">
                    <div class="modal-body p-0">
                      <div class="p-5 text-center">
                        <CheckCircleIcon class="w-16 h-16 text-success mx-auto mt-3" />
                        <div class="text-3xl mt-5">Ticket enviado correctamente!</div>
                        <div class="text-slate-500 mt-2">Presiona el boton para continuar</div>
                      </div>
                      <div class="px-5 pb-8 text-center">
                        <button type="button" data-tw-dismiss="modal" class="btn btn-primary w-24">Ok</button>
                      </div>
                    </div>
                  </div>
                </div>
              </div>
              <!-- END: Overlapping Modal Content -->
            </div>
          </div>
        </div>
      </div>
    </div>


    <!-- BEGIN: Chat Active -->
    <div v-if="chatBox" class="h-full flex flex-col">
      <div class="flex flex-col sm:flex-row border-b border-slate-200/60 dark:border-darkmode-400 px-5 py-4">
        <div class="flex items-center">
          <div class="w-10 h-10 sm:w-12 sm:h-12 flex-none image-fit relative">
          </div>
        </div>
      </div>
    </div>

    <!-- BEGIN: Chat Content -->

    <!-- END: Modal Content -->
  </div>
</template>


<script setup>
import { ref, provide } from "vue";
import { reactive, toRefs } from "vue";
import {
  required,
  minLength,
  maxLength,
} from "@vuelidate/validators";
import { useVuelidate } from "@vuelidate/core";
import Toastify from "toastify-js";
import dom from "@left4code/tw-starter/dist/js/dom";


const formData = reactive({
  RFC: "",
  comment: "",
});

const rules = {

  RFC: {
    required,
    maxLength: maxLength(13),
  },
  comment: {
    required,
    minLength: minLength(10),
  },
};

const validate = useVuelidate(rules, toRefs(formData));

const save = () => {
  validate.value.$touch();
  if (validate.value.$invalid) {
    Toastify({
      node: dom("#failed-notification-content")
        .clone()
        .removeClass("hidden")[0],
      duration: 3000,
      newWindow: true,
      close: true,
      gravity: "top",
      position: "right",
      stopOnFocus: true,
    }).showToast();
  } else {
    Toastify({
      node: dom("#success-notification-content")
        .clone()
        .removeClass("hidden")[0],
      duration: 3000,
      newWindow: true,
      close: true,
      gravity: "top",
      position: "right",
      stopOnFocus: true,
    }).showToast();
  }
};



const chatBox = ref(false);
const showChatBox = () => {
  chatBox.value = !chatBox.value;
};

const announcementRef = ref();

provide("bind[announcementRef]", (el) => {
  announcementRef.value = el;
});


</script>