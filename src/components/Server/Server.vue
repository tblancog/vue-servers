<template>
  <li
    class="list-group-item"
    style="cursor: pointer"
    v-on:click="serverSelected">
      Server #{{ server.id }}
  </li>
</template>

<script>
import { serverBus } from '../../main'
export default{
  props: ['server'],
  methods: {
    serverSelected(){
      // emit
      serverBus.$emit('serverWasSelected', this.server)

    }
  }
}
</script>

<style>

</style>
