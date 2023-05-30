<template>
  <button :type="props.ButtonInfo.type" @click="newEmit">{{ props.ButtonInfo.title }}</button>
</template>
<script setup lang="ts">

const props = defineProps({
  ButtonInfo: {
    type: Object,
    default: function () {
      return {
        title: '张三',
        type: 'sss'
      }
    }
  }
})
const emitInfo = defineEmits(['getInfo', 'ggg']);
const newEmit = () => {
  emitInfo('getInfo', 'hhh');
  emitInfo('ggg', 'hhh')
}
</script>