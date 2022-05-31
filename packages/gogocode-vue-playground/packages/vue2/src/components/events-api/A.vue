<template>
  <div>
    A:
    <button @click="inc">inc</button>
  </div>
</template>
<script>
import eventHub from './EventHub'
import TinyEmmitterBus from './utils/tiny-emitter-bus.js'

export default {
  mixins: [TinyEmmitterBus],
  methods: {
    inc() {
      eventHub.$emit('inc')
    }
  }
}
</script>
