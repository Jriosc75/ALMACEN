<script>
export default {
  props: {
    buttonText: { type: String, default: '' },
    bgColor: { type: String, default: 'black' }
  }
}
</script>

<template>
  <v-btn
    v-bind="$attrs"
    :color="bgColor"
    width="100%"
    class="py-4 white--text"
    v-on="$listeners"
  >
    {{ buttonText }}
  </v-btn>
</template>

<style>

</style>
