<template>
  <div class="p-field">
    <label for="street-input">Street: </label>
    <InputText :value="street" @input="changeStreet" id="street-input" type="text" />
  </div>
  <div class="p-field">
    <label for="state-input">State: </label>
    <InputText :value="state" @input="changeState" id="state-input" type="email" />
  </div>
  <div class="p-field">
    <label for="zip-input">Zip: </label>
    <InputText :value="zip" @input="changeZip" id="zip-input" type="number" />
  </div>
</template>

<script>
import InputText from 'primevue/inputtext'

export default {
  components: {
    InputText
  },
  props: {
    street: String,
    state: String,
    zip: Number
  },
  emits: [
    'update:street',
    'update:state',
    'update:zip'
  ],
  methods: {
    changeStreet (e) {
      this.$emit('update:street', e.target.value)
    },
    changeState (e) {
      this.$emit('update:state', e.target.value)
    },
    changeZip (e) {
      this.$emit('update:zip', e.target.value)
    }
  }
}
</script>
