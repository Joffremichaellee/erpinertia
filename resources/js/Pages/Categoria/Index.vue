<template>
    <app-layout title="Categoria">
        <template #header>
            <h2 class="font-semibold text-xl text-gray-800 leading-tight">
                Categorias
            </h2>
        </template>

        <div class="py-0">
            <div class="max-w-8xl w-full mx-auto ">
                <div class=" overflow-hidden sm:rounded-lg p-10">
                    <div class="intro-y flex items-center mt-8">
                        <Link :href="route('categoria.create')" class="btn btn-elevated-rounded-primary mr-1 mb-2">
                            <svg xmlns="http://www.w3.org/2000/svg" class="icon icon-tabler icon-tabler-circle-plus" width="28" height="28" viewBox="0 0 24 24" stroke-width="1.5" stroke="#ffffff" fill="none" stroke-linecap="round" stroke-linejoin="round">
                                <path stroke="none" d="M0 0h24v24H0z" fill="none"/>
                                <circle cx="12" cy="12" r="9" />
                                <line x1="9" y1="12" x2="15" y2="12" />
                                <line x1="12" y1="9" x2="12" y2="15" />
                            </svg>&nbsp;Nueva Categoria&nbsp;
                        </Link>
                    </div>
                    <div class="grid grid-cols-12 gap-6 mt-5">
                        <div class="intro-y col-span-12 lg:col-span-12">
                            <!-- BEGIN: Form Validation -->
                            <div class="intro-y box">
                                <div class="flex flex-col sm:flex-row items-center p-5 border-b border-gray-200 dark:border-dark-5">
                                    <h2 class="font-medium text-base mr-auto">Lista de Categorias</h2>
                                </div>
                                <div id="form-validation" class="p-5">
                                    <div class="preview">
                                        <!-- BEGIN: Validation Form -->

                                   <categoria-data :categorias="categorias" />
                                    



                                    </div>
                                    
                                </div>
                            </div>
                            <!-- END: Form Validation -->
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </app-layout>
</template>

<script>
    import { Head, Link } from '@inertiajs/inertia-vue3'
    import { defineComponent } from 'vue'
    import AppLayout from '@/Layouts/AppLayout.vue'
    import CategoriaData from '@/Components/CategoriaData.vue'


    export default defineComponent({
        mounted(){
            this.tabla();
        },
        data() {
            return {
                id: 0,
                nombre:'',
                descripcion:'',
                password:''
            }
        },
        props:['categorias'],
        components: {
            AppLayout,
            Head,
            Link,
            CategoriaData,
        },
        methods: {
            tabla(){
                $(document).ready( function () {
                    $("#table_id").DataTable({
                        "responsive": true, "lengthChange": true, "autoWidth": false
                    });
                });
            },
            EliminarCategoria(){
                Inertia.delete('/categoria/',cateogrias.id)
                .then(function (response) {
                    console.log(response);
                    window.location = '/categoria';                    
                });
            }
            /*EliminarCategoria: function (data) {
                data._method = 'DELETE';
                this.$inertia.post('/categoria/' + data.id, data)
                //$('#table_id').dataTable().fnDestroy();
                //$('#table_id').dataTable().fnClearTable();
                //$('#table_id').dataTable().fnDestroy();
                if ( $.fn.dataTable.isDataTable( '#table_id' ) ) {
                    table = $('#table_id').DataTable();
                }
                


               
            }*/
        }
    })
</script>

