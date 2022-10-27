<template>
  <div>
    <v-container cols="10" class="mx-auto">
      <h1>VISTA PRINCIPAL</h1>

      <div class="d-flex justify-space-between mt-10">
        <h1>
          GESTION DE GABINETES
        </h1>
        <v-btn  @click="$router.push({path: '/box/homeBox'})">
          GABINETES
        </v-btn>
      </div>

      <v-row class="d-flex justify-center">
        <v-col md="4" col="12">
          <div class="container-div ma-auto mt-10">
            <h1 class="container-title" >12</h1>
            <div>
              <p class="container-text red d-flex justify-center mb-5 ">Gabinetes Simples</p>
            </div>
          </div>
        </v-col>
        <v-col md="4" col="12">
          <div class="container-div ma-auto mt-10">
            <h1 class="container-title" >12</h1>
            <div>
              <p class="container-text red d-flex justify-center mb-5 ">Gabinetes Dobles</p>
            </div>
          </div>
        </v-col>
        <v-col md="4" col="12">
          <div class="container-div ma-auto mt-10">
            <h1 class="container-title" >12</h1>
            <div>
              <p class="container-text red d-flex justify-center mb-5 ">Gabinetes Triples</p>
            </div>
          </div>
        </v-col>
        <v-col md="4" col="12">
          <div class="container-div ma-auto mt-10">
            <h1 class="container-title" >12</h1>
            <div>
              <p class="container-text red d-flex justify-center mb-5 ">Gabinetes Cuadruples</p>
            </div>
          </div>
        </v-col>
        <v-col md="4" col="12">
          <div class="container-div ma-auto mt-10">
            <h1 class="container-title" >12</h1>
            <div>
              <p class="container-text red d-flex justify-center mb-5 ">Gabinetes SS2</p>
            </div>
          </div>
        </v-col>
      </v-row>
    </v-container>
    <v-container cols="10" class="mx-auto mt-10">
      <div class="d-flex justify-space-between">
        <h1>
          GESTION DE MATERIALES
        </h1>
        <v-btn  @click="$router.push({path: '/materials/homeMaterial'})">
          MATERIALES
        </v-btn>
      </div>
      <div>
        <h4 class="text-center">
          LISTA DE MATERIALES
        </h4>
        <v-card>
          <v-card-title>
            <v-text-field
              v-model="search"
              append-icon="mdi-magnify"
              label="Search"
              single-line
              hide-details
            ></v-text-field>
          </v-card-title>
          <v-data-table
            :headers="headers"
            :items="desserts"
            :search="search"
          ></v-data-table>
        </v-card>
      </div>
    </v-container>
  </div>
</template>

<script>
export default {
  data () {
    return {
      search: '',
      headers: [
        {
          text: 'Dessert (100g serving)',
          align: 'start',
          filterable: false,
          value: 'name'
        },
        { text: 'Calories', value: 'calories' }
      ],
      desserts: [
        {
          name: 'Frozen Yogurt',
          calories: 159
        },
        {
          name: 'Ice cream sandwich',
          calories: 237
        },
        {
          name: 'Eclair',
          calories: 262
        },
        {
          name: 'Cupcake',
          calories: 305
        },
        {
          name: 'Gingerbread',
          calories: 356
        },
        {
          name: 'Jelly bean',
          calories: 375
        },
        {
          name: 'Lollipop',
          calories: 392
        },
        {
          name: 'Honeycomb',
          calories: 408
        },
        {
          name: 'Donut',
          calories: 452
        },
        {
          name: 'KitKat',
          calories: 518
        }
      ]
    }
  }
}
</script>

<style scoped>
  .container-div{
    margin-top: 30px;
    background: green;
    width: 250px;
    height: 135px;
    position: relative;
  }
  .container-title{
    position:relative;
    margin: 0px auto 0px auto;
    top:-30px;
    background-color: red;
    width: 100px;
    height: 100px;
    display: flex;
    justify-content: center;
    align-items: center;
    border-radius: 100%;
    font-size: 52px;
  }
  .container-text{
    position: relative;
    top: -10px
  }
</style>
