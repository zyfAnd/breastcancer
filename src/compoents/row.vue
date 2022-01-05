<template>
  <thread
    :key="thread.id"
    :node="thread.node"
    :title="thread.title"
    :last_modified="thread.last_modified"
    :replies="thread.replies"
    :tid="thread.id"
    :member="thread.member"
  />
</template>

<script>
import Thread from './thread.vue'
export default {
  components: {
    'thread': Thread
  },
  props: ['index', 'data', 'css'],
  computed:{
    thread(){
      return this.data[this.index]
    }
  }
}
</script>
