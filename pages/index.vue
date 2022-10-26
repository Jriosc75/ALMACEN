<template>
  <div class="w-100 h-100 my-auto">
    <v-card width="400" class="ma-auto">
      <h1>ESTE ES EL LOGIN</h1>
      <v-form>
        <base-input label="Correo electronico"  />
        <base-input label="Contraseña" typeInput="password" />
        <base-button buttonText="INGRESAR"  to="dashboard/home-garage"/>
      </v-form>
    </v-card>
  </div>
</template>

<script>
import BaseButton from '../components/ui/BaseButton.vue'
import BaseInput from '../components/ui/BaseInput.vue'
export default {
  components: { BaseInput, BaseButton },
  name: 'IndexPage'
}
</script>
