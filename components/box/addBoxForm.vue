<template>
    <v-dialog  v-model="dialog" max-width="400px">
        <v-card>
            <h1>AGREGAR GABINETES AL ALMACEN</h1>
            <base-input-secondary label="SIMPLE" />
            <base-input-secondary label="DOBLES" />
            <base-input-secondary label="TRIPLES" />
            <base-input-secondary label="CUADRUPES" />
            <base-input-secondary label="SS2" />
            <v-card-actions>
                <base-button  buttonText="AGREGAR GABINETES"/>
            </v-card-actions>
        </v-card>
    </v-dialog>
</template>

<script>
import { ref } from 'vue'
import BaseInputSecondary from '../../components/ui/BaseInputSecondary.vue'
import BaseButton from '../ui/BaseButton.vue'

export default ({
  components: { BaseInputSecondary, BaseButton },

  setup () {
    const open = () => { dialog.value = true }
    const close = () => { dialog.value = false }
    const dialog = ref(false)

    return {
      open,
      close,
      dialog
    }
  }
})
</script>

<style>

</style>
