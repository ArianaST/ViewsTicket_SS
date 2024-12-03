<template>
  <div class="col-span-12 mt-8">
          <div class="intro-y flex items-center h-10">
            <h2 class="text-lg font-medium truncate mr-5">Mis tickets</h2>
            <a href="" class="ml-auto flex items-center text-primary">
              <RefreshCcwIcon class="w-4 h-4 mr-3" /> Recargar
            </a>
  </div>
  </div>
  <div class="grid grid-cols-9 gap-6 mt-2">
            <div class="col-span-14 sm:col-span-8 xl:col-span-3 intro-y">
              <div class="report-box zoom-in">
                <div class="box p-5">
                  <div class="flex">
                    <CheckCircleIcon class="report-box__icon text-success" />
                    <div class="ml-auto">
                      <Tippy
                        tag="div"
                        class="report-box__indicator bg-success cursor-pointer" >
                        33%
                        <CheckCircleIcon class="w-4 h-4 ml-0.5" />
                      </Tippy>
                    </div>
                  </div>
                  <div class="text-3xl font-medium leading-8 mt-6">4</div>
                  <div class="text-base text-slate-500 mt-1">Tickets completos</div>
                </div>
              </div>
            </div>
            <div class="col-span-12 sm:col-span-6 xl:col-span-3 intro-y">
              <div class="report-box zoom-in">
                <div class="box p-5">
                  <div class="flex">
                    <LoadingIcon icon="bars" color="orange" class="report-box__icon" />
                    <div class="ml-auto">
                      <Tippy
                        tag="div"
                        class="report-box__indicator bg-warning" >
                        2%
                        <BarChart2Icon class="w-4 h-4 ml-0.5" />
                      </Tippy>
                    </div>
                  </div>
                  <div class="text-3xl font-medium leading-8 mt-6">2</div>
                  <div class="text-base text-slate-500 mt-1">Tickets en progreso</div>
                </div>
              </div>
            </div>
            <div class="col-span-12 sm:col-span-6 xl:col-span-3 intro-y">
              <div class="report-box zoom-in">
                <div class="box p-5">
                  <div class="flex">
                    <XCircleIcon class="report-box__icon text-danger"/>
                    <div class="ml-auto">
                      <Tippy
                        tag="div"
                        class="report-box__indicator bg-danger">
                        12% <XCircleIcon class="w-4 h-4 ml-0.5" />
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
            <div  class="col-span-12 sm:col-span-6 xl:col-span-3 intro-y">
              <div class="report-box zoom-in">
                <div class="box p-5">
                  <div class="flex">
                    <PlusCircleIcon class="report-box__icon text-primary" />
                    <div class="ml-auto">
                      <Tippy
                        tag="div"
                        class="report-box__indicator bg-primary">
                        22% <PlusIcon class="w-4 h-4 ml-0.5" />
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
            <div class="col-span-12 sm:col-span-6 xl:col-span-3 intro-y">
              <div class="report-box zoom-in">
                <div class="box p-5">
                  <div class="flex">
                    <LoadingIcon icon="rings" color="grey" class="report-box__icon" />
                    <div class="ml-auto">
                      <Tippy
                        tag="div"
                        class="report-box__indicator bg-slate-500 cursor-pointer">
                        12% <PackageIcon class="w-4 h-4 ml-0.5" />
                      </Tippy>
                    </div>
                  </div>
                  <div class="text-3xl font-medium leading-8 mt-6">0</div>
                  <div class="text-base text-slate-500 mt-1">
                    Tickets recibidos
                  </div>
                </div>
              </div>
            </div>
            <div class="col-span-12 sm:col-span-6 xl:col-span-3 intro-y">
              <div class="report-box zoom-in">
                <div class="box p-5">
                  <div class="flex">
                    <AlertTriangleIcon class="report-box__icon text-pending" />
                    <div class="ml-auto">
                      <Tippy
                        tag="div"
                        class="report-box__indicator bg-pending cursor-pointer"
                      >
                        22% <AlertTriangleIcon class="w-4 h-4 ml-0.5" />
                      </Tippy>
                    </div>
                  </div>
                  <div class="text-3xl font-medium leading-8 mt-6">1</div>
                  <div class="text-base text-slate-500 mt-1">
                    Tickets rechazados
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
              <button
                class="nav-link w-full py-2 active"
                data-tw-toggle="pill"
                data-tw-target="#chats"
                type="button"
                role="tab"
                aria-controls="chats"
                aria-selected="true"
              >
                Chats
              </button>
            </li>
            <li id="friends-tab" class="nav-item flex-1" role="presentation">
              <button
                class="nav-link w-full py-2"
                data-tw-toggle="pill"
                data-tw-target="#friends"
                type="button"
                role="tab"
                aria-controls="friends"
                aria-selected="false"
              >
                Tickets
              </button>
            </li>
            <li id="profile-tab" class="nav-item flex-1" role="presentation">
              <button
                class="nav-link w-full py-2"
                data-tw-toggle="pill"
                data-tw-target="#profile"
                type="button"
                role="tab"
                aria-controls="profile"
                aria-selected="false"
              >
                Profile
              </button>
            </li>
          </ul>
        </div>
      </div>
      <div class="tab-content">
        <div
          id="chats"
          class="tab-pane active"
          role="tabpanel"
          aria-labelledby="chats-tab"
        >
          <div class="pr-1">
            <div class="box px-5 pt-5 pb-5 lg:pb-0 mt-5">
              <div class="relative text-slate-500">
                <input
                  type="text"
                  class="form-control py-3 px-4 border-transparent bg-slate-100 pr-10"
                  placeholder="Search for messages or users..."
                />
                <SearchIcon
                  class="w-4 h-4 hidden sm:absolute my-auto inset-y-0 mr-3 right-0"
                />
              </div>
              <div class="overflow-x-auto scrollbar-hidden">
                <div class="flex mt-5">
                  <a
                    v-for="(faker, fakerKey) in $_.take($f(), 10)"
                    :key="fakerKey"
                    href=""
                    class="w-10 mr-4 cursor-pointer"
                  >
                    <div class="w-10 h-10 flex-none image-fit rounded-full">
                      <img
                        alt="Rubick Tailwind HTML Admin Template"
                        class="rounded-full"
                        :src="faker.photos[0]"
                      />
                      <div
                        class="w-3 h-3 bg-success absolute right-0 bottom-0 rounded-full border-2 border-white dark:border-darkmode-600"
                      ></div>
                    </div>
                    <div
                      class="text-xs text-slate-500 truncate text-center mt-2"
                    >
                      {{ faker.users[0].name }}
                    </div>
                  </a>
                </div>
              </div>
            </div>
          </div>
          <div
            class="chat__chat-list overflow-y-auto scrollbar-hidden pr-1 pt-1 mt-4"
          >
            <div
              v-for="(faker, fakerKey) in $_.take($f(), 10)"
              :key="fakerKey"
              class="intro-x cursor-pointer box relative flex items-center p-5"
              :class="{ 'mt-5': fakerKey }"
              @click="showChatBox"
            >
              <div class="w-12 h-12 flex-none image-fit mr-1">
                <img
                  alt="Rubick Tailwind HTML Admin Template"
                  class="rounded-full"
                  :src="faker.photos[0]"
                />
                <div
                  class="w-3 h-3 bg-success absolute right-0 bottom-0 rounded-full border-2 border-white dark:border-darkmode-600"
                ></div>
              </div>
              <div class="ml-2 overflow-hidden">
                <div class="flex items-center">
                  <a href="javascript:;" class="font-medium">{{
                    faker.users[0].name
                  }}</a>
                  <div class="text-xs text-slate-400 ml-auto">
                    {{ faker.times[0] }}
                  </div>
                </div>
                <div class="w-full truncate text-slate-500 mt-0.5">
                  {{ faker.news[0].shortContent }}
                </div>
              </div>
              <div
                v-if="faker.trueFalse[0]"
                class="w-5 h-5 flex items-center justify-center absolute top-0 right-0 text-xs text-white rounded-full bg-primary font-medium -mt-1 -mr-1"
              >
                {{ faker.notificationCount }}
              </div>
            </div>
          </div>
        </div>
        <div
          id="friends"
          class="tab-pane"
          role="tabpanel"
          aria-labelledby="friends-tab"
        >
        <br>
        <div class="intro-y col-span-12 lg:col-span-8">
      <div class="lg:flex intro-y">
        <div class="relative">
          <input
            type="text"
            class="form-control py-3 px-4 w-full lg:w-45 box pr-0"
            placeholder="Buscar ticket..."
          />
          <SearchIcon
            class="w-4 h-4 absolute my-auto inset-y-0 mr-3 right-0 text-slate-500"
          />
        </div>
        <select
          class="form-select py-2 px-2 box w-full lg:w-auto mt-2 lg:mt-0 ml-auto"
        >
          <option>Ordenar por</option>
          <option>A a la Z</option>
          <option>Z a la A</option>
          <option>Proximos a vencer</option>
        </select>
      </div>
        </div>

          <div
            class="chat__user-list overflow-y-auto scrollbar-hidden pr-1 pt-1"
          >
            <div class="mt-4 text-slate-500">Tickets proximos a vencer</div>
            <div class="cursor-pointer box relative flex items-center p-5 mt-5">
              <div class="w-10 h-10 flex-none image-fit mr-1">
                <LayersIcon class="report-box__icon text-primary"></LayersIcon>
                <div class="progress mt-2">
    <div class="progress-bar w-3/4 bg-warning" role="progressbar" aria-valuenow="0" aria-valuemin="0" aria-valuemax="50"></div>
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
    <div class="progress-bar w-3/4 bg-warning" role="progressbar" aria-valuenow="0" aria-valuemin="0" aria-valuemax="50"></div>
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
    <div class="progress-bar w-2/3 bg-success" role="progressbar" aria-valuenow="0" aria-valuemin="0" aria-valuemax="100"></div>
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
    <div class="progress-bar w-2/3 bg-success" role="progressbar" aria-valuenow="0" aria-valuemin="0" aria-valuemax="100"></div>
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
    <div class="progress-bar w-2/3 bg-success" role="progressbar" aria-valuenow="0" aria-valuemin="0" aria-valuemax="100"></div>
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

            <div  class="chat__user-list overflow-y-auto scrollbar-hidden pr-1 pt-1">
            <div class="mt-4 text-slate-500">Tickets cancelados</div>
            <div class="cursor-pointer box relative flex items-center p-5 mt-5">
              <div class="w-12 h-12 flex-none image-fit mr-1">
                <div class="w-9 h-9 flex-none image-fit mr-1">
                <LayersIcon class="report-box__icon text-primary" />
                <div class="progress mt-3">
                  <div class="progress-bar w-4/4 bg-danger" role="progressbar" aria-valuenow="0" aria-valuemin="0" aria-valuemax="100"></div>
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
                <a
                  class="dropdown-toggle w-5 h-5 block"
                  aria-expanded="false"
                  data-tw-toggle="dropdown"
                > </a>
                <div>
                  <button  href="javascript:;" data-tw-toggle="modal" data-tw-target="#overlapping-modal-preview20"><Trash2Icon class="w-5 h-5 text-slate-500"/> </button>
                </div>
            <!-- BEGIN: Modal Toggle -->
            <div id="overlapping-modal-preview20" class="modal" data-tw-backdrop="static"  tabindex="-1" aria-hidden="true">

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
            <button
              type="button"
              data-tw-dismiss="modal"
              class="btn btn-outline-secondary w-24 mr-1"
            >
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
        <div
          id="profile"
          class="tab-pane"
          role="tabpanel"
          aria-labelledby="profile-tab"
        >
          <div class="pr-1">
            <div class="box px-5 py-10 mt-5">
              <div
                class="w-20 h-20 flex-none image-fit rounded-full overflow-hidden mx-auto"
              >
                <img
                  alt="Rubick Tailwind HTML Admin Template"
                  :src="$f()[0].photos[0]"
                />
              </div>
              <div class="text-center mt-3">
                <div class="font-medium text-lg">
                  {{ $f()[0]["users"][0]["name"] }}
                </div>
                <div class="text-slate-500 mt-1">
                  Tailwind HTML Admin Template
                </div>
              </div>
            </div>
            <div class="box p-5 mt-5">
              <div
                class="flex items-center border-b border-slate-200/60 dark:border-darkmode-400 pb-5"
              >
                <div>
                  <div class="text-slate-500">Country</div>
                  <div class="mt-1">New York City, USA</div>
                </div>
                <GlobeIcon class="w-4 h-4 text-slate-500 ml-auto" />
              </div>
              <div
                class="flex items-center border-b border-slate-200/60 dark:border-darkmode-400 py-5"
              >
                <div>
                  <div class="text-slate-500">Phone</div>
                  <div class="mt-1">+32 19 23 62 24 34</div>
                </div>
                <MicIcon class="w-4 h-4 text-slate-500 ml-auto" />
              </div>
              <div
                class="flex items-center border-b border-slate-200/60 dark:border-darkmode-400 py-5"
              >
                <div>
                  <div class="text-slate-500">Email</div>
                  <div class="mt-1">{{ $f()[0]["users"][0]["email"] }}</div>
                </div>
                <MailIcon class="w-4 h-4 text-slate-500 ml-auto" />
              </div>
              <div class="flex items-center pt-5">
                <div>
                  <div class="text-slate-500">Joined Date</div>
                  <div class="mt-1">{{ $f()[0]["dates"][0] }}</div>
                </div>
                <ClockIcon class="w-4 h-4 text-slate-500 ml-auto" />
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>

    <!-- END: Chat Side Menu -->
    <!-- BEGIN: Chat Content -->

    <div class="intro-y col-span-12 lg:col-span-8 2xl:col-span-9">
      <div class="chat__box box">
    
    <!--GRIND1 END-->
  <div class="grid grid-cols-20 gap-35 mt-0">
    
    <button class="col-span-12 sm:col-span-6 xl:col-span-3 intro-y">
                  <a href="javascript:;" data-tw-toggle="modal" data-tw-target="#overlapping-modal-problem">
                    <div id="overlapping-modal-problem" class="modal"  tabindex="-1" aria-hidden="true">
                      <div class="modal-dialog modal-xl">
                      <div class="modal-content">
                        <div class="modal-header">
                          <div class="text-center">
                        <h2 class="font-medium text-base ">Información</h2>
                        </div>
                        <div>
                          <InfoIcon class="w-5 h-5 ml-8" />
                        </div>
                        
    <div text="center"
      class="relative before:hidden before:lg:block before:absolute before:w-[60%] before:h-[4px] before:top-0 before:bottom-0 before:mt-4 before:bg-slate-900 before:dark:bg-darkmode-500 flex flex-col lg:flex-row dark:bg-flex-row-400 dark:border-darkmode-700 justify-center px-30 sm:px-20">
      <div class="intro-x lg:text-center flex items-right lg:block flex-1 z-2" >
        
        <button class="w-10 h-10 rounded-full btn btn-primary">1</button>
        
        <div class="lg:w-32 font-medium text-base lg:mt-3 ml-3 lg:mx-auto">Nuevo
        </div>
      </div>
      <div class="intro-x lg:text-center flex items-center mt-5 lg:mt-0 lg:block flex-1 z-10">
        <button class="w-10 h-10 rounded-full btn btn-primary">
          2
        </button>
        <div class="lg:w-32 font-medium text-base lg:mt-3 ml-3 lg:mx-auto">
          Recibido
        </div>
      </div>
      <div
        class="intro-x lg:text-center flex items-center lg:block flex-1 z-10">
        <button
          class="w-10 h-10 rounded-full btn btn-primary"
        >
          3
        </button>
        <div
          class="lg:w-32 font-medium text-base lg:mt-3 ml-3 lg:mx-auto"
        >
          En progreso
        </div>
      </div>
      <div
        class="intro-x lg:text-center flex items-center mt-5 lg:mt-0 lg:block flex-1 z-10" >
        <button
          class=" w-10 h-10 rounded-full btn btn-primary" 
        > <LoadingIcon icon="puff" color="white" class=" h-5 ml-0" />
        </button>
        <div
          class="lg:w-32 font-medium text-base lg:mt-3 ml-3 lg:mx-auto"
        > 
       Completado
        </div>
      </div>
    </div>
    </div>

                        <div class="modal-body grid grid-cols-12 gap-4 gap-y-3" @submit.prevent="save"> 
            <div class="col-span-12 sm:col-span-12">
              <label for="horizontal-form-1" class="form-label" >Problema</label>
              <input
                id="horizontal-form-1"
                type="text"
                class="form-control"
                placeholder="Reportes en altas tickets"
                  :value="$f()[0].users[0].$message"
                  disabled
              />
              </div>

              <div class="col-span-12 sm:col-span-12">
                <label
                  for="validation-form-6"
                  class="form-label w-full flex flex-col sm:flex-row">
                   Descipción
                </label>
                <textarea
                  id="validation-form-6"
                  class="form-control"
                  name="comment"
                  placeholder="Descripcion del problema"
                  :value="$f()[0].users[0].$message"
                  disabled
                ></textarea>
              </div>

              <div class="col-span-12 sm:col-span-12">
              <label for="regular-form-3" class="form-label">Nombre del solicitante</label>
              <input
                id="regular-form-3"
                type="text"
                class="form-control"
                placeholder="Input text"
                  :value="$f()[0].users[0].name"
                  disabled
              />
           </div>
           <div class="col-span-12 sm:col-span-12">
                <label for="regular-form-4" class="form-label">Email</label>
                <input
                 id="regular-form-4" 
                 type="text" 
                 class="form-control" 
                 placeholder="Input text"
                  :value="$f()[0].users[0].email"
                  disabled
                 />
            </div> 
            <div class="col-span- sm:col-span-12">
              <label for="regular-form-5" class="form-label">Nombre de la empresa </label>
              <input
                id="regular-form-5"
                type="text"
                class="form-control"
                placeholder="Ingresa el nombrre de la empresa"
                :value="$f()[0].users[0].$message"
                  disabled
              />
            </div>
            <div class="col-span-12 sm:col-span-12">
                <label
                  for="validation-form-4"
                  class="form-label w-full flex flex-col sm:flex-row"
                >
                  RFC
                </label>
                <input
                  id="validation-form-4"
                  type="text"
                  name="rfc"
                  class="form-control"
                  placeholder="TAJI090411OJA"
                  :value="$f()[0].users[0].$message"
                  disabled
                />
            </div>
                 <div class="modal-footer">
                    <a href="javascript:;" data-tw-toggle="modal" data-tw-target="#next-overlapping-modal-preview2" type="submit" class=" btn btn-danger shadow-md w-30 mr-6 mb-2">  <Trash2Icon class="w-4 h-4 mr-2" /> Eliminar</a>
                    </div>
                        </div>
                </div>
                <div id="next-overlapping-modal-preview2" data-tw-backdrop="static" class="modal" tabindex="-1" aria-hidden="true">
                    <div class="modal-dialog">
                        <div class="modal-content">
                          <div class="modal-body p-0">
                <div class="p-5 text-center">
                  <XCircleIcon class="w-16 h-16 text-warning mx-auto mt-3" />
                    <div class="text-3xl mt-5">Warning</div>
                    <div class="text-slate-500 mt-2">¿Estas seguro que quieres borrar este ticket?</div>
                </div>
                <div class="modal-footer text-right">
                    <button type="button" data-tw-dismiss="modal"  class="btn btn-danger shadow-md w-24 mr-1">Sí</button>
                    <button type="button" data-tw-dismiss="modal" class="btn btn-primary shadow-md w-24 mr-1">No</button>
                  </div>
                          </div>
                        </div>
                    </div>
                </div>
                      </div>
                      </div>      
            <div class="col-span-12 sm:col-span-6 xl:col-span-3 intro-x">
              <div class="report-box zoom-in">
                <div class="box p-5">
                  <div class="flex">

                    <LayersIcon class="report-box__icon text-primary" />
                    <div class="ml-auto">
                      <Tippy
                        tag="div"
                        class="report-box__indicator bg-success cursor-pointer"
                        content="Completado"
                      >
                       Completado
                        <ChevronUpIcon class="w-4 h-4 ml-0.5" />
                      </Tippy>
                    </div>
                  </div>
                  <div class="text-3xl font-medium leading-8 mt-6">Nombre del problema</div>
                  <div class="text-base text-slate-500 mt-1">Descripción</div>
                </div>
              </div>
            </div>
          </a>
          </button>
      </div>
      <!--GRIND1 FINISH-->  


        <!----GRIND2 END---->
        <div class="grid grid-cols-20 gap-6 mt-5">
    <button class="col-span-12 sm:col-span-6 2xl:col-span-3 intro-y">
                  <a href="javascript:;" data-tw-toggle="modal" data-tw-target="#overlapping-modal-problem5">
                    <div id="overlapping-modal-problem5" class="modal"  tabindex="-1" aria-hidden="true">
                      <div class="modal-dialog modal-xl" >
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
      <div
        class="intro-x lg:text-center flex items-center lg:block flex-1 z-10"
      >
        <button class="w-10 h-10 rounded-full btn btn-primary">1</button>
        <div class="lg:w-32 font-medium text-base lg:mt-3 ml-3 lg:mx-auto">
          Nuevo
        </div>
      </div>
      <div
        class="intro-x lg:text-center flex items-center mt-5 lg:mt-0 lg:block flex-1 z-10"
      >
        <button
          class="w-10 h-10 rounded-full btn btn-primary"
        >
          2
        </button>
        <div
          class="lg:w-32 font-medium text-base lg:mt-3 ml-3 lg:mx-auto"
        >
          Recibido
        </div>
      </div>
      <div
        class="intro-x lg:text-center flex items-center mt-5 lg:mt-0 lg:block flex-1 z-10"
      >
        <button
          class="w-10 h-10 rounded-full btn btn-primary"
        >
        <LoadingIcon icon="puff" color="white" class=" h-5 ml-0" />
        </button>
        <div
          class="lg:w-32 font-medium text-base lg:mt-3 ml-3 lg:mx-auto"
        >
          En progreso
        </div>
      </div>
      <div
        class="intro-x lg:text-center flex items-center mt-5 lg:mt-0 lg:block flex-1 z-10"
      >
        <button
          class="w-10 h-10 rounded-full btn text-slate-500 bg-slate-100 dark:bg-darkmode-400 dark:border-darkmode-400"
        >
          4
        </button>
        <div
          class="lg:w-32 text-base lg:mt-3 ml-3 lg:mx-auto text-slate-600 dark:text-slate-400"
        >
       Completado
        </div>
      </div>
    </div>
   

                        </div>
                        <div class="modal-body grid grid-cols-12 gap-4 gap-y-3" @submit.prevent="save"> 
            <div class="col-span-12 sm:col-span-12">
              <label for="horizontal-form-1" class="form-label" >Problema</label>
              <input
                id="horizontal-form-1"
                type="text"
                class="form-control"
                placeholder="Reportes en altas tickets"
                  :value="$f()[0].users[0].$message"
                  disabled
              />
              </div>

              <div class="col-span-12 sm:col-span-12">
                <label
                  for="validation-form-6"
                  class="form-label w-full flex flex-col sm:flex-row">
                   Descipción
                </label>
                <textarea
                  id="validation-form-6"
                  class="form-control"
                  name="comment"
                  placeholder="Descripcion del problema"
                  :value="$f()[0].users[0].$message"
                  disabled
                ></textarea>
              </div>

              <div class="col-span-12 sm:col-span-12">
              <label for="regular-form-3" class="form-label">Nombre del solicitante</label>
              <input
                id="regular-form-3"
                type="text"
                class="form-control"
                placeholder="Input text"
                  :value="$f()[0].users[0].name"
                  disabled
              />
           </div>
           <div class="col-span-12 sm:col-span-12">
                <label for="regular-form-4" class="form-label">Email</label>
                <input
                 id="regular-form-4" 
                 type="text" 
                 class="form-control" 
                 placeholder="Input text"
                  :value="$f()[0].users[0].email"
                  disabled
                 />
            </div> 
            <div class="col-span-12 sm:col-span-12">
              <label for="regular-form-5" class="form-label">Nombre de la empresa </label>
              <input
                id="regular-form-5"
                type="text"
                class="form-control"
                placeholder="Ingresa el nombrre de la empresa"
                :value="$f()[0].users[0].$message"
                  disabled
              />
            </div>
            <div class="col-span-12 sm:col-span-12">
                <label
                  for="validation-form-4"
                  class="form-label w-full flex flex-col sm:flex-row"
                >
                  RFC
                </label>
                <input
                  id="validation-form-4"
                  type="text"
                  name="rfc"
                  class="form-control"
                  placeholder="TAJI090411OJA"
                  :value="$f()[0].users[0].$message"
                  disabled
                />
            </div>
                                 <div class="modal-footer">
                    <a href="javascript:;" data-tw-toggle="modal" data-tw-target="#next-overlapping-modal-preview5" type="submit" class=" btn btn-danger shadow-md w-30 mr-6 mb-2">  <SlashIcon class="w-4 h-4 mr-2" />Cancelar</a>
                    </div>
                        </div>
                </div>
                <div id="next-overlapping-modal-preview5" data-tw-backdrop="static" class="modal" tabindex="-1" aria-hidden="true">
                    <div class="modal-dialog">
                        <div class="modal-content">
                          <div class="modal-body p-0">
                <div class="p-5 text-center">
                  <XCircleIcon class="w-16 h-16 text-warning mx-auto mt-3" />
                    <div class="text-3xl mt-5">Warning</div>
                    <div class="text-slate-500 mt-2">¿Estas seguro que quieres cancelar este ticket?</div>
                </div>
                <div class="modal-footer text-right">
                    <button type="button" data-tw-dismiss="modal"  class="btn btn-danger shadow-md w-24 mr-1">Sí</button>
                    <button type="button" data-tw-dismiss="modal" class="btn btn-primary shadow-md w-24 mr-1">No</button>
                  </div>
                          </div>
                        </div>
                    </div>
                </div>
                      </div>
                      </div>      
            <div class="col-span-12 sm:col-span-6 xl:col-span-3 intro-x">
              <div class="report-box zoom-in">
                <div class="box p-5">
                  <div class="flex">
                    <LayersIcon class="report-box__icon text-primary" />
                    <div class="ml-auto">
                      <Tippy
                        tag="div"
                        class="report-box__indicator bg-warning cursor-pointer"
                        content="En progreso"
                      >
                      En progreso
                        <ChevronUpIcon class="w-4 h-4 ml-0.5" />
                      </Tippy>
                    </div>
                  </div>
                  <div class="text-3xl font-medium leading-8 mt-6">Nombre del problema</div>
                  <div class="text-base text-slate-500 mt-1">Descripción</div>
                </div>
              </div>
            </div>
          </a>
          </button>
      </div>
      <!--GRIND2 FINISH-->


      <!----GRIND3 END-->
      <div class="grid grid-cols-20 gap-6 mt-5">
    <button class="col-span-12 sm:col-span-6 xl:col-span-3 intro-y">
                  <a href="javascript:;" data-tw-toggle="modal" data-tw-target="#overlapping-modal-problem10">
                    <div id="overlapping-modal-problem10" class="modal"  tabindex="-1" aria-hidden="true">
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
      <div
        class="intro-x lg:text-center flex items-center lg:block flex-1 z-10"
      >
        <button class="w-10 h-10 rounded-full btn btn-primary">1</button>
        <div class="lg:w-32 font-medium text-base lg:mt-3 ml-3 lg:mx-auto">
          Nuevo
        </div>
      </div>
      <div
        class="intro-x lg:text-center flex items-center mt-5 lg:mt-0 lg:block flex-1 z-10"
      >
        <button
          class="w-10 h-10 rounded-full btn btn-primary"
        >
          2
        </button>
        <div
          class="lg:w-32 font-medium text-base lg:mt-3 ml-3 lg:mx-auto"
        >
          Recibido
        </div>
      </div>
      <div
        class="intro-x lg:text-center flex items-center mt-5 lg:mt-0 lg:block flex-1 z-10"
      >
        <button
          class="w-10 h-10 rounded-full btn btn-primary"
        >
          3
        </button>
        <div
          class="lg:w-32 font-medium text-base lg:mt-3 ml-3 lg:mx-auto"
        >
          En progreso
        </div>
      </div>
      <div
        class="intro-x lg:text-center flex items-center mt-5 lg:mt-0 lg:block flex-1 z-10"
      >
        <button
          class="w-10 h-10 rounded-full btn btn-primary"
        >
        <LoadingIcon icon="puff" color="white" class=" h-5 ml-0" />
        </button>
        <div
          class="lg:w-32 font-medium text-base lg:mt-3 ml-3 lg:mx-auto"
        >
         Cancelado
        </div>
      </div>
    </div>

                        </div>
                        <div class="modal-body grid grid-cols-12 gap-4 gap-y-3" @submit.prevent="save"> 
            <div class="col-span-12 sm:col-span-12">
              <label for="horizontal-form-1" class="form-label" >Problema</label>
              <input
                id="horizontal-form-1"
                type="text"
                class="form-control"
                placeholder="Reportes en altas tickets"
                  :value="$f()[0].users[0].$message"
                  disabled
              />
              </div>

              <div class="col-span-12 sm:col-span-12">
                <label
                  for="validation-form-6"
                  class="form-label w-full flex flex-col sm:flex-row">
                   Descipción
                </label>
                <textarea
                  id="validation-form-6"
                  class="form-control"
                  name="comment"
                  placeholder="Descripcion del problema"
                  :value="$f()[0].users[0].$message"
                  disabled
                ></textarea>
              </div>

              <div class="col-span-12 sm:col-span-12">
              <label for="regular-form-3" class="form-label">Nombre del solicitante</label>
              <input
                id="regular-form-3"
                type="text"
                class="form-control"
                placeholder="Input text"
                  :value="$f()[0].users[0].name"
                  disabled
              />
           </div>
           <div class="col-span-12 sm:col-span-12">
                <label for="regular-form-4" class="form-label">Email</label>
                <input
                 id="regular-form-4" 
                 type="text" 
                 class="form-control" 
                 placeholder="Input text"
                  :value="$f()[0].users[0].email"
                  disabled
                 />
            </div> 
            <div class="col-span-12 sm:col-span-12">
              <label for="regular-form-5" class="form-label">Nombre de la empresa </label>
              <input
                id="regular-form-5"
                type="text"
                class="form-control"
                placeholder="Ingresa el nombrre de la empresa"
                :value="$f()[0].users[0].$message"
                  disabled
              />
            </div>
            <div class="col-span-12 sm:col-span-12">
                <label
                  for="validation-form-4"
                  class="form-label w-full flex flex-col sm:flex-row"
                >
                  RFC
                </label>
                <input
                  id="validation-form-4"
                  type="text"
                  name="rfc"
                  class="form-control"
                  placeholder="TAJI090411OJA"
                  :value="$f()[0].users[0].$message"
                  disabled
                />
            </div>

                        </div>
                </div>
                <br>
                <div class="alert alert-danger alert-dismissible show flex items-center mb-2" role="alert">
    <AlertOctagonIcon class="w-6 h-6 mr-2" /> Este ticket se encuentra cancelado
    
       
</div>
                <div id="next-overlapping-modal-preview6" data-tw-backdrop="static" class="modal" tabindex="-1" aria-hidden="true">
                    <div class="modal-dialog">
                        <div class="modal-content">
                          <div class="modal-body p-0">
                <div class="p-5 text-center">
                  <XCircleIcon class="w-16 h-16 text-warning mx-auto mt-3" />
                    <div class="text-3xl mt-5">Warning</div>
                    <div class="text-slate-500 mt-2">¿Estas seguro que quieres cancelar este ticket?</div>
                </div>
                <div class="modal-footer text-right">
                    <button type="button" data-tw-dismiss="modal"  class="btn btn-danger shadow-md w-24 mr-1">Sí</button>
                    <button type="button" data-tw-dismiss="modal" class="btn btn-primary shadow-md w-24 mr-1">No</button>
                  </div>
                          </div>
                        </div>
                    </div>
                </div>
                      </div>
                      </div>      
            <div class="col-span-12 sm:col-span-6 xl:col-span-3 intro-y">
              <div class="report-box zoom-in">
                <div class="box p-5">
                  <div class="flex">
                    <LayersIcon class="report-box__icon text-primary" />
                    <div class="ml-auto">
                      <Tippy
                        tag="div"
                        class="report-box__indicator bg-danger cursor-pointer"
                        content="Cancelado"
                      >
                      Cancelado   
                        <ChevronUpIcon class="w-4 h-4 ml-0.5" />
                      </Tippy>
                    </div>
                  </div>
                  <div class="text-3xl font-medium leading-8 mt-6">Nombre del problema</div>
                  <div class="text-base text-slate-500 mt-1">Descripción</div>
                </div>
              </div>
            </div>
          </a>
          </button>
      </div>
        <!----GRIND3 FINISH-->


   <!----GRIND4 END-->
        <div class="grid grid-cols-20 gap-6 mt-5">
    <button class="col-span-12 sm:col-span-6 xl:col-span-3 intro-y">
                  <a href="javascript:;" data-tw-toggle="modal" data-tw-target="#overlapping-modal-problem7">
                    <div id="overlapping-modal-problem7" class="modal"  tabindex="-1" aria-hidden="true">
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

<div
        class="intro-x lg:text-center flex items-center lg:block flex-1 z-10"
      >
        <button class="w-10 h-10 rounded-full btn btn-primary">
          <LoadingIcon icon="puff" color="white" class=" h-5 ml-0" />
        </button>
        <div class="lg:w-32 font-medium text-base lg:mt-3 ml-3 lg:mx-auto">
          Nuevo
        </div>
      </div>
      <div
        class="intro-x lg:text-center flex items-center mt-5 lg:mt-0 lg:block flex-1 z-10"
      >
        <button
          class="w-10 h-10 rounded-full btn text-slate-500 bg-slate-100 dark:bg-darkmode-400 dark:border-darkmode-400"
        >
          2
        </button>
        <div
          class="lg:w-32 text-base lg:mt-3 ml-3 lg:mx-auto text-slate-600 dark:text-slate-400"
        >
          Recibido
        </div>
      </div>
      <div
        class="intro-x lg:text-center flex items-center mt-5 lg:mt-0 lg:block flex-1 z-10"
      >
        <button
          class="w-10 h-10 rounded-full btn text-slate-500 bg-slate-100 dark:bg-darkmode-400 dark:border-darkmode-400"
        >
          3
        </button>
        <div
          class="lg:w-32 text-base lg:mt-3 ml-3 lg:mx-auto text-slate-600 dark:text-slate-400"
        >
          En progreso
        </div>
      </div>
      <div
        class="intro-x lg:text-center flex items-center mt-5 lg:mt-0 lg:block flex-1 z-10"
      >
        <button
          class="w-10 h-10 rounded-full btn text-slate-500 bg-slate-100 dark:bg-darkmode-400 dark:border-darkmode-400"
        >
          4
        </button>
        <div
          class="lg:w-32 text-base lg:mt-3 ml-3 lg:mx-auto text-slate-600 dark:text-slate-400"
        >
       Completado
        </div>
      </div>
    </div>

                        </div>
                        <div class="modal-body grid grid-cols-12 gap-4 gap-y-3" @submit.prevent="save"> 
            <div class="col-span-12 sm:col-span-12">
              <label for="horizontal-form-1" class="form-label" >Problema</label>
              <input
                id="horizontal-form-1"
                type="text"
                class="form-control"
                placeholder="Reportes en altas tickets"
                  :value="$f()[0].users[0].$message"
                  disabled
              />
              </div>

              <div class="col-span-12 sm:col-span-12">
                <label
                  for="validation-form-6"
                  class="form-label w-full flex flex-col sm:flex-row">
                   Descipción
                </label>
                <textarea
                  id="validation-form-6"
                  class="form-control"
                  name="comment"
                  placeholder="Descripcion del problema"
                  :value="$f()[0].users[0].$message"
                  disabled
                ></textarea>
              </div>

              <div class="col-span-12 sm:col-span-12">
              <label for="regular-form-3" class="form-label">Nombre del solicitante</label>
              <input
                id="regular-form-3"
                type="text"
                class="form-control"
                placeholder="Input text"
                  :value="$f()[0].users[0].name"
                  disabled
              />
           </div>
           <div class="col-span-12 sm:col-span-12">
                <label for="regular-form-4" class="form-label">Email</label>
                <input
                 id="regular-form-4" 
                 type="text" 
                 class="form-control" 
                 placeholder="Input text"
                  :value="$f()[0].users[0].email"
                  disabled
                 />
            </div> 
            <div class="col-span-12 sm:col-span-12">
              <label for="regular-form-5" class="form-label">Nombre de la empresa </label>
              <input
                id="regular-form-5"
                type="text"
                class="form-control"
                placeholder="Ingresa el nombrre de la empresa"
                :value="$f()[0].users[0].$message"
                  disabled
              />
            </div>
            <div class="col-span-12 sm:col-span-12">
                <label
                  for="validation-form-4"
                  class="form-label w-full flex flex-col sm:flex-row"
                >
                  RFC
                </label>
                <input
                  id="validation-form-4"
                  type="text"
                  name="rfc"
                  class="form-control"
                  placeholder="TAJI090411OJA"
                  :value="$f()[0].users[0].$message"
                  disabled
                />
            </div>
                                 <div class="modal-footer">
                    <a href="javascript:;" data-tw-toggle="modal" data-tw-target="#next-overlapping-modal-preview7" type="submit" class=" btn btn-danger shadow-md w-30 mr-6 mb-2">  <SlashIcon class="w-4 h-4 mr-2" /> Cancelar</a>
                    </div>
                        </div>
                </div>
                <div id="next-overlapping-modal-preview7" data-tw-backdrop="static" class="modal" tabindex="-1" aria-hidden="true">
                    <div class="modal-dialog">
                        <div class="modal-content">
                          <div class="modal-body p-0">
                <div class="p-5 text-center">
                  <XCircleIcon class="w-16 h-16 text-warning mx-auto mt-3" />
                    <div class="text-3xl mt-5">Warning</div>
                    <div class="text-slate-500 mt-2">¿Estas seguro que cancelar cancelar este ticket?</div>
                </div>
                <div class="modal-footer text-right">
                    <button type="button" data-tw-dismiss="modal"  class="btn btn-danger shadow-md w-24 mr-1">Sí</button>
                    <button type="button" data-tw-dismiss="modal" class="btn btn-primary shadow-md w-24 mr-1">No</button>
                  </div>
                          </div>
                        </div>
                    </div>
                </div>
                      </div>
                      </div> 

            <div class="col-span-12 sm:col-span-6 xl:col-span-3 intro-y">
              <div class="report-box zoom-in">
                <div class="box p-5">
                  <div class="flex">
                    <LayersIcon class="report-box__icon text-primary" />
                    <div class="ml-auto">
                      <Tippy
                        tag="div"
                        class="report-box__indicator bg-primary cursor-pointer"
                        content="Nuevo"
                      >
                     Nuevo
                        <ChevronUpIcon class="w-4 h-4 ml-0.5" />
                      </Tippy>
                    </div>
                  </div>
                  <div class="text-3xl font-medium leading-8 mt-6">Nombre del problema</div>
                  <div class="text-base text-slate-500 mt-1">Descripción</div>
                </div>
              </div>
            </div>
          </a>
          </button>
        </div>
<!----GRIND4 FINISH-->


<div class="grid grid-cols-20 gap-6 mt-5">
    <button class="col-span-12 sm:col-span-6 xl:col-span-3 intro-y">
                  <a href="javascript:;" data-tw-toggle="modal" data-tw-target="#overlapping-modal-problem11">
                    <div id="overlapping-modal-problem11" class="modal"  tabindex="-1" aria-hidden="true">
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
      <div
        class="intro-x lg:text-center flex items-center lg:block flex-1 z-10"
      >
        <button class="w-10 h-10 rounded-full btn btn-primary">1</button>
        <div class="lg:w-32 font-medium text-base lg:mt-3 ml-3 lg:mx-auto">
          Nuevo
        </div>
      </div>
      <div
        class="intro-x lg:text-center flex items-center mt-5 lg:mt-0 lg:block flex-1 z-10"
      >
        <button
          class="w-10 h-10 rounded-full btn btn-primary"
        >
        <LoadingIcon icon="puff" color="white" class=" h-5 ml-0" />
        </button>
        <div
          class="lg:w-32 font-medium text-base lg:mt-3 ml-3 lg:mx-auto"
        >
          Recibido
        </div>
      </div>
      <div
        class="intro-x lg:text-center flex items-center mt-5 lg:mt-0 lg:block flex-1 z-10"
      >
        <button
          class="w-10 h-10 rounded-full btn text-slate-500 bg-slate-100 dark:bg-darkmode-400 dark:border-darkmode-400"
        >
          3
        </button>
        <div
          class="lg:w-32 text-base lg:mt-3 ml-3 lg:mx-auto text-slate-600 dark:text-slate-400"
        >
          En progreso
        </div>
      </div>
      <div
        class="intro-x lg:text-center flex items-center mt-5 lg:mt-0 lg:block flex-1 z-10"
      >
        <button
          class="w-10 h-10 rounded-full btn text-slate-500 bg-slate-100 dark:bg-darkmode-400 dark:border-darkmode-400"
        >
          4
        </button>
        <div
          class="lg:w-32 text-base lg:mt-3 ml-3 lg:mx-auto text-slate-600 dark:text-slate-400"
        >
       Completado
        </div>
      </div>
    </div>

                        </div>
                        <div class="modal-body grid grid-cols-12 gap-4 gap-y-3" @submit.prevent="save"> 
            <div class="col-span-12 sm:col-span-12">
              <label for="horizontal-form-1" class="form-label" >Problema</label>
              <input
                id="horizontal-form-1"
                type="text"
                class="form-control"
                placeholder="Reportes en altas tickets"
                  :value="$f()[0].users[0].$message"
                  disabled
              />
              </div>

              <div class="col-span-12 sm:col-span-12">
                <label
                  for="validation-form-6"
                  class="form-label w-full flex flex-col sm:flex-row">
                   Descipción
                </label>
                <textarea
                  id="validation-form-6"
                  class="form-control"
                  name="comment"
                  placeholder="Descripcion del problema"
                  :value="$f()[0].users[0].$message"
                  disabled
                ></textarea>
              </div>

              <div class="col-span-12 sm:col-span-12">
              <label for="regular-form-3" class="form-label">Nombre del solicitante</label>
              <input
                id="regular-form-3"
                type="text"
                class="form-control"
                placeholder="Input text"
                  :value="$f()[0].users[0].name"
                  disabled
              />
           </div>
           <div class="col-span-12 sm:col-span-12">
                <label for="regular-form-4" class="form-label">Email</label>
                <input
                 id="regular-form-4" 
                 type="text" 
                 class="form-control" 
                 placeholder="Input text"
                  :value="$f()[0].users[0].email"
                  disabled
                 />
            </div> 
            <div class="col-span-12 sm:col-span-12">
              <label for="regular-form-5" class="form-label">Nombre de la empresa </label>
              <input
                id="regular-form-5"
                type="text"
                class="form-control"
                placeholder="Ingresa el nombrre de la empresa"
                :value="$f()[0].users[0].$message"
                  disabled
              />
            </div>
            <div class="col-span-12 sm:col-span-12">
                <label
                  for="validation-form-4"
                  class="form-label w-full flex flex-col sm:flex-row"
                >
                  RFC
                </label>
                <input
                  id="validation-form-4"
                  type="text"
                  name="rfc"
                  class="form-control"
                  placeholder="TAJI090411OJA"
                  :value="$f()[0].users[0].$message"
                  disabled
                />
            </div>
                                 <div class="modal-footer">
                    <a href="javascript:;" data-tw-toggle="modal" data-tw-target="#next-overlapping-modal-preview11" type="submit" class=" btn btn-danger shadow-md w-30 mr-6 mb-2">  <SlashIcon class="w-4 h-4 mr-2" /> Cancelar</a>
                    </div>
                        </div>
                </div>
                <div id="next-overlapping-modal-preview11" data-tw-backdrop="static" class="modal" tabindex="-1" aria-hidden="true">
                    <div class="modal-dialog">
                        <div class="modal-content">
                          <div class="modal-body p-0">
                <div class="p-5 text-center">
                  <XCircleIcon class="w-16 h-16 text-warning mx-auto mt-3" />
                    <div class="text-3xl mt-5">Warning</div>
                    <div class="text-slate-500 mt-2">¿Estas seguro que cancelar cancelar este ticket?</div>
                </div>
                <div class="modal-footer text-right">
                    <button type="button" data-tw-dismiss="modal"  class="btn btn-danger shadow-md w-24 mr-1">Sí</button>
                    <button type="button" data-tw-dismiss="modal" class="btn btn-primary shadow-md w-24 mr-1">No</button>
                  </div>
                          </div>
                        </div>
                    </div>
                </div>
                      </div>
                      </div> 

            <div class="col-span-12 sm:col-span-6 xl:col-span-3 intro-y">
              <div class="report-box zoom-in">
                <div class="box p-5">
                  <div class="flex">
                    <LayersIcon class="report-box__icon text-primary" />
                    <div class="ml-auto">
                      <Tippy
                        tag="div"
                        class="report-box__indicator bg-slate-500 cursor-pointer"
                        content="Recibido"
                      >
                      Recibido
                        <ChevronUpIcon class="w-4 h-4 ml-0.5" />
                      </Tippy>
                    </div>
                  </div>
                  <div class="text-3xl font-medium leading-8 mt-6">Nombre del problema</div>
                  <div class="text-base text-slate-500 mt-1">Descripción</div>
                </div>
              </div>
            </div>
          </a>
          </button>
</div>

<!----GRIND5 END--->


<div class="grid grid-cols-20 gap-6 mt-5">
    <button class="col-span-12 sm:col-span-6 xl:col-span-3 intro-y">
                  <a href="javascript:;" data-tw-toggle="modal" data-tw-target="#overlapping-modal-problem12">
                    <div id="overlapping-modal-problem12" class="modal"  tabindex="-1" aria-hidden="true">
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
      <div
        class="intro-x lg:text-center flex items-center lg:block flex-1 z-10"
      >
        <button class="w-10 h-10 rounded-full btn btn-primary">1</button>
        <div class="lg:w-32 font-medium text-base lg:mt-3 ml-3 lg:mx-auto">
          Nuevo
        </div>
      </div>
      <div
        class="intro-x lg:text-center flex items-center mt-5 lg:mt-0 lg:block flex-1 z-10"
      >
        <button
          class="w-10 h-10 rounded-full btn btn-primary"
        >
          2
        </button>
        <div
          class="lg:w-32 font-medium text-base lg:mt-3 ml-3 lg:mx-auto"
        >
          Recibido
        </div>
      </div>
      <div
        class="intro-x lg:text-center flex items-center mt-5 lg:mt-0 lg:block flex-1 z-10"
      >
        <button
          class="w-10 h-10 rounded-full btn btn-primary"
        >
          3
        </button>
        <div
          class="lg:w-32 font-medium text-base lg:mt-3 ml-3 lg:mx-auto"
        >
          En progreso
        </div>
      </div>
      <div
        class="intro-x lg:text-center flex items-center mt-5 lg:mt-0 lg:block flex-1 z-10"
      >
        <button
          class="w-10 h-10 rounded-full btn btn-primary"
        > <LoadingIcon icon="puff" color="white" class=" h-5 ml-0" />
          
        </button>
        <div
          class="lg:w-32 font-medium text-base lg:mt-3 ml-3 lg:mx-auto"
        >
       Rechazado
        </div>
      </div>
    </div>

                        </div>
                        <div class="modal-body grid grid-cols-12 gap-4 gap-y-3" @submit.prevent="save"> 
            <div class="col-span-12 sm:col-span-12">
              <label for="horizontal-form-1" class="form-label" >Problema</label>
              <input
                id="horizontal-form-1"
                type="text"
                class="form-control"
                placeholder="Reportes en altas tickets"
                  :value="$f()[0].users[0].$message"
                  disabled
              />
              </div>

              <div class="col-span-12 sm:col-span-12">
                <label
                  for="validation-form-6"
                  class="form-label w-full flex flex-col sm:flex-row">
                   Descipción
                </label>
                <textarea
                  id="validation-form-6"
                  class="form-control"
                  name="comment"
                  placeholder="Descripcion del problema"
                  :value="$f()[0].users[0].$message"
                  disabled
                ></textarea>
              </div>

              <div class="col-span-12 sm:col-span-12">
              <label for="regular-form-3" class="form-label">Nombre del solicitante</label>
              <input
                id="regular-form-3"
                type="text"
                class="form-control"
                placeholder="Input text"
                  :value="$f()[0].users[0].name"
                  disabled
              />
           </div>
           <div class="col-span-12 sm:col-span-12">
                <label for="regular-form-4" class="form-label">Email</label>
                <input
                 id="regular-form-4" 
                 type="text" 
                 class="form-control" 
                 placeholder="Input text"
                  :value="$f()[0].users[0].email"
                  disabled
                 />
            </div> 
            <div class="col-span-12 sm:col-span-12">
              <label for="regular-form-5" class="form-label">Nombre de la empresa </label>
              <input
                id="regular-form-5"
                type="text"
                class="form-control"
                placeholder="Ingresa el nombrre de la empresa"
                :value="$f()[0].users[0].$message"
                  disabled
              />
            </div>
            <div class="col-span-12 sm:col-span-12">
                <label
                  for="validation-form-4"
                  class="form-label w-full flex flex-col sm:flex-row"
                >
                  RFC
                </label>
                <input
                  id="validation-form-4"
                  type="text"
                  name="rfc"
                  class="form-control"
                  placeholder="TAJI090411OJA"
                  :value="$f()[0].users[0].$message"
                  disabled
                />
            </div>
                                 <div class="modal-footer">
                    <a href="javascript:;" data-tw-toggle="modal" data-tw-target="#next-overlapping-modal-preview12" type="submit" class=" btn btn-danger shadow-md w-30 mr-6 mb-2">  <SlashIcon class="w-4 h-4 mr-2" /> Cancelar</a>
                    </div>
                        </div>
                </div>
                <div id="next-overlapping-modal-preview12" data-tw-backdrop="static" class="modal" tabindex="-1" aria-hidden="true">
                    <div class="modal-dialog">
                        <div class="modal-content">
                          <div class="modal-body p-0">
                <div class="p-5 text-center">
                  <XCircleIcon class="w-16 h-16 text-warning mx-auto mt-3" />
                    <div class="text-3xl mt-5">Warning</div>
                    <div class="text-slate-500 mt-2">¿Estas seguro que cancelar cancelar este ticket?</div>
                </div>
                <div class="modal-footer text-right">
                    <button type="button" data-tw-dismiss="modal"  class="btn btn-danger shadow-md w-24 mr-1">Sí</button>
                    <button type="button" data-tw-dismiss="modal" class="btn btn-primary shadow-md w-24 mr-1">No</button>
                  </div>
                          </div>
                        </div>
                    </div>
                </div>
                      </div>
                      </div> 

            <div class="col-span-12 sm:col-span-6 xl:col-span-3 intro-y">
              <div class="report-box zoom-in">
                <div class="box p-5">
                  <div class="flex">
                    <LayersIcon class="report-box__icon text-primary" />
                    <div class="ml-auto">
                      <Tippy
                        tag="div"
                        class="report-box__indicator bg-pending cursor-pointer"
                        content="Rechazado"
                      >
                      Rechazado
                        <ChevronUpIcon class="w-4 h-4 ml-0.5" />
                      </Tippy>
                    </div>
                  </div>
                  <div class="text-3xl font-medium leading-8 mt-6">Nombre del problema</div>
                  <div class="text-base text-slate-500 mt-1">Descripción</div>
                </div>
              </div>
            </div>
          </a>
          </button>
          <!---GRND5 FINISH --->

                    <!-- BEGIN: Modal Toggle -->
                    <div>
                  <a href="javascript:;" data-tw-toggle="modal" data-tw-target="#overlapping-modal-preview" class="btn btn-rounded-primary shadow-md "> <PlusCircleIcon class="w-9 h-9 "/> </a>
                </div>
            <!-- BEGIN: Modal Toggle -->
            <div id="overlapping-modal-preview" class="modal" data-tw-backdrop="static"  tabindex="-1" aria-hidden="true">
              <div class="modal-dialog ">
              <div class="modal-content">
                <div class="intro-y box py-1100 sm:py-100 mt-100">
                </div>
                
              <!-- END: Modal Header -->
                <div class="modal-header"> 
                <h2 class="font-medium text-base mr-auto">Levantar ticket</h2>
                <button class="btn btn-outline-secondary hidden sm:flex">
                    <FileIcon class="w-3 h-3 mr-2" /> Download Docs
                  <input
                    type="file"
                    class=" absolute opacity-0"
                  />
                </button>
                </div>
            <div class="modal-body grid grid-cols-12 gap-4 gap-y-3" @submit.prevent="save"> 
            <div class="col-span-12 sm:col-span-12">
              <label for="horizontal-form-1" class="form-label" >Problema</label>
              <input
                id="horizontal-form-1"
                type="text"
                class="form-control"
                placeholder="Ingresa el problema"
              />
              </div>

              <div class="col-span-12 sm:col-span-12">
                <label
                  for="validation-form-6"
                  class="form-label w-full flex flex-col sm:flex-row">
                   Descipción
                  <span class="sm:ml-auto mt-1 sm:mt-0 text-xs text-slate-500">
                    al menos 10 caracteres</span>
                </label>
                <textarea
                  id="validation-form-6"
                  v-model.trim="validate.comment.$model"
                  class="form-control"
                  :class="{ 'border-danger': validate.comment.$error }"
                  name="comment"
                  placeholder="Escribe la descripcion del problema"
                ></textarea>
                <template v-if="validate.comment.$error">
                  <div
                    v-for="(error, index) in validate.comment.$errors"
                    :key="index"
                    class="text-danger mt-2">
                    {{ error.$message }}
                  </div>
                </template>
              </div>
              <div class="col-span-12 sm:col-span-12">
              <label for="regular-form-3" class="form-label">Nombre del solicitante</label>
              <input
                id="regular-form-3"
                type="text"
                class="form-control"
                placeholder="Ej.Abisai Gomez Peralta"
              />
           </div>
           <div class="col-span-12 sm:col-span-12">
                <label for="regular-form-4" class="form-label">Email</label>
                <input
                 id="regular-form-4" 
                 type="text" 
                 class="form-control" 
                 placeholder="example@gmail.com"
                 />
            </div> 
            <div class="col-span-12 sm:col-span-12">
              <label for="regular-form-5" class="form-label">Nombre de la empresa </label>
              <input
                id="regular-form-5"
                type="text"
                class="form-control"
                placeholder="Ingresa el nombrre de la empresa"
              />
            </div>
            <div class="col-span-12 sm:col-span-12">
                <label
                  for="validation-form-4"
                  class="form-label w-full flex flex-col sm:flex-row"
                >
                  RFC
                  <span class="sm:ml-auto mt-1 sm:mt-0 text-xs text-slate-500"
                    >Requiere 13 caracteres</span
                  >
                </label>
                <input
                  id="validation-form-4"
                  v-model.trim="validate.RFC.$model"
                  type="text"
                  name="rfc"
                  class="form-control"
                  :class="{ 'border-danger': validate.RFC.$error }"
                  placeholder="TAJI090411OJA"
                />
                <template v-if="validate.RFC.$error">
                  <div
                    v-for="(error, index) in validate.RFC.$errors"
                    :key="index"
                    class="text-danger mt-2"
                  >
                    {{ error.$message }}
                  </div>
                </template>
            
            </div>
            

   
                    <!-- BEGIN: Overlapping Modal Toggle -->
                    <div class="modal-footer" >
                    <button type="button" href="javascript:;" data-tw-toggle="modal" data-tw-target="#next-overlapping-modal-preview"  data-tw-dismiss="modal"  class="btn btn-elevated-secondary w-24 mr-0 mb-2">Enviar</button>
                    <button type="button" data-tw-dismiss="modal" class="btn btn-elevated-primary w-24 mb-0">Cerrar</button>
                 
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


        <!-- BEGIN: Chat Active -->
        <div v-if="chatBox" class="h-full flex flex-col">
          <div
            class="flex flex-col sm:flex-row border-b border-slate-200/60 dark:border-darkmode-400 px-5 py-4"
          >
            <div class="flex items-center">
              <div
                class="w-10 h-10 sm:w-12 sm:h-12 flex-none image-fit relative"
              >
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>

  


 <!-- BEGIN: Chat Content -->
<br><br><br><br><br><br><br><br><br><br><br><br><br><br>

        <!-- BEGIN: Chat Active -->
        <div v-if="chatBox" class="h-full flex flex-col">
          <div
            class="flex flex-col sm:flex-row border-b border-slate-200/60 dark:border-darkmode-400 px-5 py-4"
          >
            <div class="flex items-center">
              <div
                class="w-10 h-10 sm:w-12 sm:h-12 flex-none image-fit relative"
              >
                <img
                  alt="Rubick Tailwind HTML Admin Template"
                  class="rounded-full"
                  :src="$f()[0].photos[0]"
                />
              </div>
              <div class="ml-3 mr-auto">
                <div class="font-medium text-base">
                  {{ $f()[0]["users"][0]["name"] }}
                </div>
                <div class="text-slate-500 text-xs sm:text-sm">
                  Hey, I am using chat <span class="mx-1">•</span> Online
                </div>
              </div>
            </div>
            <div
              class="flex items-center sm:ml-auto mt-5 sm:mt-0 border-t sm:border-0 border-slate-200/60 pt-3 sm:pt-0 -mx-5 sm:mx-0 px-5 sm:px-0"
            >
              <a href="javascript:;" class="w-5 h-5 text-slate-500">
                <SearchIcon class="w-5 h-5" />
              </a>
              <a href="javascript:;" class="w-5 h-5 text-slate-500 ml-5">
                <UserPlusIcon class="w-5 h-5" />
              </a>
              <div class="dropdown ml-auto sm:ml-3">
                <a
                  href="javascript:;"
                  class="dropdown-toggle w-5 h-5 text-slate-500"
                  aria-expanded="false"
                  data-tw-toggle="dropdown"
                >
                  <MoreVerticalIcon class="w-5 h-5" />
                </a>
                <div class="dropdown-menu w-40">
                  <ul class="dropdown-content">
                    <li>
                      <a href="" class="dropdown-item">
                        <Share2Icon class="w-4 h-4 mr-2" />
                        Share Contact
                      </a>
                    </li>
                    <li>
                      <a href="" class="dropdown-item">
                        <SettingsIcon class="w-4 h-4 mr-2" />
                        Settings
                      </a>
                    </li>
                  </ul>
                </div>
              </div>
            </div>
          </div>
        </div>


<!-- END: Modal Content -->
  </div>
</template>


<script setup>
import { ref } from "vue";
import { reactive, toRefs } from "vue";
import {
  required,
  minLength,
  maxLength,
} from "@vuelidate/validators";
import { useVuelidate } from "@vuelidate/core";
import Toastify from "toastify-js";
import dom from "@left4code/tw-starter/dist/js/dom";
import VueDatePicker from '@vuepic/vue-datepicker';


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

</script>