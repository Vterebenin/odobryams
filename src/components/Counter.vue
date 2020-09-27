<template lang="pug">
button(@click="addMoreOdobryams")
  | count is: {{ state.count  }}
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
      state.count++
    }

    return {
      state,
      addMoreOdobryams
    }
  }
}
</script>
