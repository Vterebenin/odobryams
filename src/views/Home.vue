<template lang="pug">
img(src="@/assets/theCat.png")
h2 The one and only:
h1 Odobryams counter!
counter
</template>

<script>
// @ is an alias to /src
import Counter from '@/components/Counter'

export default {
  name: 'Home',
  components: { Counter }
}
</script>
