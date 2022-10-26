<script>
export default {
  props: {
    label: { type: String, default: '' },
    typeInput: { type: String, default: 'text' },
    bgColor: { type: String, default: '' }
  }
}
</script>

<template>
  <div class="d-flex justify-space-between align-start base">
    <v-text-field
      v-bind="$attrs"
      class="base__textfield"
      :label="label"
      :background-color="bgColor"
      :type="typeInput"
      filled
      dense
      v-on="$listeners"
      hide-spin-buttons
    />
  </div>
</template>

<style lang="scss" scoped>
.base {
  margin-top: -15px;
  &__label {
    max-width: 100px;
    &__text{
      color: black;
      font-size: 18px;
      font-weight: 300;
      margin-left: 8px;
    }
  }
  &__textfield {
    max-width: 200px;
    margin-right: 12px;
  }
}
</style>
