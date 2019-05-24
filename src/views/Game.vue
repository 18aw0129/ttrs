<template>
  <div class="game">
    <h1>This is an about page</h1>
    <ttrs />
  </div>
</template>


<script>
// @ is an alias to /src
import ttrs from '@/components/ttrs.vue'

export default {
  name: 'game',
  components: {
    ttrs
  }
}
</script>