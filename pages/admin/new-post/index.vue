<template>
  <div class="admin-page">
    <section class="new-post-form">
      <form @submit.prevent="onSave">
        <AppControlInput v-model="editedPost.author">Author Name:</AppControlInput>
        <AppControlInput v-model="editedPost.title">Title:</AppControlInput>
        <AppControlInput v-model="editedPost.thumbnailLink">Thumbnail Link:</AppControlInput>
        <AppControlInput control-type="textarea" v-model="editedPost.content">Content:</AppControlInput>
        
        <AppButton type="submit">Save</AppButton>
        <AppButton
          type="button"
          style="margin-left: 10px"
          btn-style="cancel"
          @click="onCancel">Cancel</AppButton>
      </form>
    </section>
  </div>
</template>

<script>
import AppControlInput from '@/components/UI/AppControlInput'
import AppButton from '@/components/UI/AppButton'

export default {
  components: {
    AppControlInput,
    AppButton
  },
  data() {
    return {
      editedPost: {
        author: '',
        title: '',
        thumbnailLink: ''
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
.admin-page {
  padding: 20px;
}

.new-post {
  text-align: center;
  border-bottom: 2px solid #ccc;
  padding-bottom: 10px;
}

.existing-posts h1 {
  text-align: center;
}
</style>