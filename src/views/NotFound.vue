<template>
  <div class="home">
    Error 404, la ruta a la que deseas acceder no existe.
  </div>
</template>

<script>
import Nprogress from 'nprogress'
export default {
  name: 'NotFound',
  async created(){
    Nprogress.done();
  }
}
</script>
