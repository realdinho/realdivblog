<template>
   <form @submit.prevent="onSave">
      <AppControlInput v-model="editedPost.author">Author Name:</AppControlInput>
      <AppControlInput v-model="editedPost.title">Title:</AppControlInput>
      <AppControlInput v-model="editedPost.thumbnail">Thumbnail Link:</AppControlInput>
      <AppControlInput control-type="textarea" v-model="editedPost.content">Content:</AppControlInput>
      
      <AppButton type="submit">Save</AppButton>
      <AppButton type="button" class="btn-cancel" btn-style="cancel" @click="onCancel">Cancel</AppButton>
  </form>
</template>

<script>
import AppControlInput from '@/components/UI/AppControlInput'
import AppButton from '@/components/UI/AppButton'

export default {
  components: {
    AppControlInput,
    AppButton
  },
  props: {
    post: {
      type: Object,
      required: false
    }
  },
  data() {
    return {
      editedPost: this.post ? { ...this.post } : {
        author: '',
        title: '',
        thumbnail: ''
      }
    }
  },
  methods: {
    onSave() {
      // save the post
      console.log(this.editedPost);
    },
    onCancel() {
      // cancel and navigate back
      this.$router.push('/admin');
    }
  }
}
</script>

<style scoped>
  .btn-cancel {
    margin-left: 10px;
  }
</style>