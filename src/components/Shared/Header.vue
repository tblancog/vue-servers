<template>
    <div class="row">
        <div class="col-xs-12">
            <header>
                <h1>Server Status <span v-if="id">#{{ id }}</span></h1>
            </header>
        </div>
    </div>
</template>

<script>
import { serverBus } from '../../main'
export default{
  data(){
    return {
      id: null
    }
  },
  created(){
    serverBus.$on('serverWasSelected', (server) => {
      this.id = server.id
      // console.log(server)
    })
  }
}
</script>

<style>

</style>
