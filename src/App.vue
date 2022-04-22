<template>
  <div style="width: 100%; height: 90%">
    <QuillEditor theme="snow" toolbar="full" v-model:content="content" contentType="html" />
  </div>
  <textarea style="width: 100%; height: 96%" v-model="content"></textarea>
</template>

<script>
import { reactive, toRefs } from 'vue'
import { QuillEditor } from '@vueup/vue-quill'
import '@vueup/vue-quill/dist/vue-quill.snow.css'

export default {
  name: 'App',
  components: {
    QuillEditor
  },
  setup () {
    const data = reactive({
      toolbar: ['bold', 'italic', 'underline', 'strike'],
      content: ''
    })

    return {
      ...toRefs(data)
    }
  }
}
</script>

<style lang="less"></style>
