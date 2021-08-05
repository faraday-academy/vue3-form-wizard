<template>
  <div class="p-field">
    <label for="name-input">Name: </label>
    <InputText :value="name" @input="changeName" id="name-input" type="text" />
  </div>
  <div class="p-field">
    <label for="email-input">E-mail: </label>
    <InputText :value="email" @input="changeEmail" id="email-input" type="email" />
  </div>
  <div class="p-field">
    <label for="phone-input">Phone: </label>
    <InputText :value="phone" @input="changePhone" id="phone-input" type="text" />
  </div>
</template>

<script>
import InputText from 'primevue/inputtext'

export default {
  components: {
    InputText
  },
  props: {
    name: String,
    email: String,
    phone: String
  },
  emits: [
    'update:name',
    'update:email',
    'update:phone'
  ],
  methods: {
    changeName (e) {
      this.$emit('update:name', e.target.value)
    },
    changeEmail (e) {
      this.$emit('update:email', e.target.value)
    },
    changePhone (e) {
      this.$emit('update:phone', e.target.value)
    }
  }
}
</script>
