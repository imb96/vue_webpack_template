<template>
  <h1>
    {{ msg }}
  </h1>
  <h2>{{ storeMsg }} / {{ storeMessage }}</h2>
  <Hello />
</template>

<script>
import Hello from '@/components/Hello'

export default {
  components: {
    Hello,
  },

  data() {
    return {
      msg: 'Hello Webpack?!'
    }
  },

  computed: {
    storeMsg() {
      return this.$store.state.msg
    },
    storeMessage() {
      return this.$store.state.message.message
    }
  }
}
</script>
