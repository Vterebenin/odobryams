<template lang="pug">
h1 {{ state.count }}
button(@click="addMoreOdobryams")
  | add another odobryams
</template>
<script>
import { reactive, computed } from 'vue'
export default {
  setup () {
    const state = reactive({
      count: 0,
      double: computed(() => state.count * 2)
    })

    const addMoreOdobryams = () => {
      const password = window.prompt('Enter the passphrase to make it!')
      password && ['ковшечка', 'ковш', 'ковшик'].includes(password.toLowerCase())
        ? state.count++
        : alert('yo! you are not the real odobryams')
    }

    return {
      state,
      addMoreOdobryams
    }
  }
}
</script>
