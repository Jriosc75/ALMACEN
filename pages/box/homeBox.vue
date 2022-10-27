<template>
  <div>
    <v-container cols="10" class="mx-auto mb-10">
        <h1>
        <v-icon>
            mdi-star
        </v-icon>
            MIS GABINETES
        </h1>

      <div class="d-flex justify-space-between mt-10">
        <h1>
          GABINETES EN ALMACEN
        </h1>
        <v-btn @click="clientInformationModal">
          AGREGAR GABINETES AL ALMACEN
        </v-btn>
      </div>

      <v-row >
        <v-col md="4" col="12">
          <div class="container-div d-flex ma-auto mt-6">
            <h1 class="container-title" >12</h1>
            <p class="container-text red d-flex justify-center ">Gabinetes Simples</p>
          </div>
        </v-col>
        <v-col md="4" col="12">
          <div class="container-div d-flex ma-auto mt-6">
            <h1 class="container-title" >12</h1>
            <p class="container-text red d-flex justify-center ">Gabinetes Dobles</p>
          </div>
        </v-col>
        <v-col md="4" col="12">
          <div class="container-div d-flex ma-auto mt-6">
            <h1 class="container-title" >12</h1>
            <p class="container-text red d-flex justify-center ">Gabinetes Triples</p>
          </div>
        </v-col>
        <v-col md="4" col="12">
          <div class="container-div d-flex ma-auto mt-6">
            <h1 class="container-title" >121</h1>
            <p class="container-text red d-flex justify-center ">Gabinetes Cuadruples</p>
          </div>
        </v-col>
        <v-col md="4" col="12">
          <div class="container-div d-flex ma-auto mt-6">
            <h1 class="container-title" >121</h1>
            <p class="container-text red d-flex justify-center ">Gabinetes Simples</p>
          </div>
        </v-col>
      </v-row>

      <div class="d-flex flex-column mt-16">
        <h1>
          GABINETES POR REPORTAR
        </h1>
        <div class="d-flex justify-space-between">
            <v-btn class="mt-4">
                AGREGAR TECNICO
            </v-btn>
            <div style="width: 340px">
                <v-autocomplete
                    w
                    v-model="model"
                    :hint="!isEditing ? 'Click the icon to edit' : 'Click the icon to save'"
                    :items="states"
                    :readonly="!isEditing"
                    :label="`State — ${isEditing ? 'Editable' : 'Readonly'}`"
                    persistent-hint
                >
                    <template v-slot:append-outer>
                    <v-slide-x-reverse-transition
                        mode="out-in"
                    >
                        <v-icon
                        :key="`icon-${isEditing}`"
                        :color="isEditing ? 'success' : 'info'"
                        @click="isEditing = !isEditing"
                        v-text="isEditing ? 'mdi-check-outline' : 'mdi-circle-edit-outline'"
                        ></v-icon>
                    </v-slide-x-reverse-transition>
                    </template>
                </v-autocomplete>
            </div>
        </div>
      </div>

      <v-row>
        <v-col md="4" col="12">
          <div class="container-div d-flex ma-auto mt-6">
            <h1 class="container-title" >12</h1>
            <p class="container-text red d-flex justify-center ">Gabinetes Simples</p>
          </div>
        </v-col>
        <v-col md="4" col="12">
          <div class="container-div d-flex ma-auto mt-6">
            <h1 class="container-title" >12</h1>
            <p class="container-text red d-flex justify-center ">Gabinetes Dobles</p>
          </div>
        </v-col>
        <v-col md="4" col="12">
          <div class="container-div d-flex ma-auto mt-6">
            <h1 class="container-title" >12</h1>
            <p class="container-text red d-flex justify-center ">Gabinetes Triples</p>
          </div>
        </v-col>
        <v-col md="4" col="12">
          <div class="container-div d-flex ma-auto mt-6">
            <h1 class="container-title" >121</h1>
            <p class="container-text red d-flex justify-center ">Gabinetes Cuadruples</p>
          </div>
        </v-col>
        <v-col md="4" col="12">
          <div class="container-div d-flex ma-auto mt-6">
            <h1 class="container-title" >121</h1>
            <p class="container-text red d-flex justify-center ">Gabinetes Simples</p>
          </div>
        </v-col>
      </v-row>

      <div class="mt-16 d-flex flex-column">
        <h1>
          GABINETES REPORTADOS
        </h1>
        <div class="d-flex justify-end">
            <div style="width: 340px">
                <v-autocomplete
                    w
                    v-model="model"
                    :hint="!isEditing ? 'Click the icon to edit' : 'Click the icon to save'"
                    :items="states"
                    :readonly="!isEditing"
                    :label="`State — ${isEditing ? 'Editable' : 'Readonly'}`"
                    persistent-hint
                >
                    <template v-slot:append-outer>
                    <v-slide-x-reverse-transition
                        mode="out-in"
                    >
                        <v-icon
                        :key="`icon-${isEditing}`"
                        :color="isEditing ? 'success' : 'info'"
                        @click="isEditing = !isEditing"
                        v-text="isEditing ? 'mdi-check-outline' : 'mdi-circle-edit-outline'"
                        ></v-icon>
                    </v-slide-x-reverse-transition>
                    </template>
                </v-autocomplete>
            </div>
        </div>
      </div>

      <v-row>
        <v-col md="4" col="12">
          <div class="container-div d-flex ma-auto mt-6">
            <h1 class="container-title" >12</h1>
            <p class="container-text red d-flex justify-center ">Gabinetes Simples</p>
          </div>
        </v-col>
        <v-col md="4" col="12">
          <div class="container-div d-flex ma-auto mt-6">
            <h1 class="container-title" >12</h1>
            <p class="container-text red d-flex justify-center ">Gabinetes Dobles</p>
          </div>
        </v-col>
        <v-col md="4" col="12">
          <div class="container-div d-flex ma-auto mt-6">
            <h1 class="container-title" >12</h1>
            <p class="container-text red d-flex justify-center ">Gabinetes Triples</p>
          </div>
        </v-col>
        <v-col md="4" col="12">
          <div class="container-div d-flex ma-auto mt-6">
            <h1 class="container-title" >121</h1>
            <p class="container-text red d-flex justify-center ">Gabinetes Cuadruples</p>
          </div>
        </v-col>
        <v-col md="4" col="12">
          <div class="container-div d-flex ma-auto mt-6">
            <h1 class="container-title" >121</h1>
            <p class="container-text red d-flex justify-center ">Gabinetes Simples</p>
          </div>
        </v-col>
      </v-row>
    </v-container>

    <add-box-form ref="openClientInformationModal"/>

  </div>
</template>

<script>
import { ref } from 'vue'
import addBoxForm from '../../components/box/addBoxForm.vue'

export default ({
  components: { addBoxForm },

  setup () {
    const isEditing = ref(false)
    const model = ref(null)
    const openClientInformationModal = ref(null)
    const clientInformationModal = () => {
      try {
        openClientInformationModal.value.open()
      } catch (e) {
        console.log(e)
      }
    }
    const states = ref([
      'Alabama', 'Alaska', 'American Samoa', 'Arizona',
      'Arkansas', 'California', 'Colorado', 'Connecticut',
      'Delaware', 'District of Columbia', 'Federated States of Micronesia',
      'Florida', 'Georgia', 'Guam', 'Hawaii', 'Idaho',
      'Illinois', 'Indiana', 'Iowa', 'Kansas', 'Kentucky',
      'Louisiana', 'Maine', 'Marshall Islands', 'Maryland',
      'Massachusetts', 'Michigan', 'Minnesota', 'Mississippi',
      'Missouri', 'Montana', 'Nebraska', 'Nevada',
      'New Hampshire', 'New Jersey', 'New Mexico', 'New York',
      'North Carolina', 'North Dakota', 'Northern Mariana Islands', 'Ohio',
      'Oklahoma', 'Oregon', 'Palau', 'Pennsylvania', 'Puerto Rico',
      'Rhode Island', 'South Carolina', 'South Dakota', 'Tennessee',
      'Texas', 'Utah', 'Vermont', 'Virgin Island', 'Virginia',
      'Washington', 'West Virginia', 'Wisconsin', 'Wyoming'
    ])

    return {
      isEditing,
      model,
      states,
      openClientInformationModal,
      clientInformationModal
    }
  }
})
</script>

<style scoped>
  .container-div{
    width: 300px;
    margin-top: 30px;
    background: green;
    position: relative;
  }
  .container-title{
    position:relative;
    left: -45px;
    background-color: red;
    width: 80px;
    height: 80px;
    display: flex;
    justify-content: center;
    align-items: center;
    border-radius: 100%;
    font-size: 36px;
  }
  .container-text{
    margin: auto 0px auto 10px;
  }
</style>
