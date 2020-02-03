<template>
  <div class="admin-post-page">
    <section class="update-form">
      <AdminPostForm :post="loadedPost" />
    </section>
  </div>
</template>

<script>
import AdminPostForm from '@/components/Admin/AdminPostForm' 

export default {
  components: {
    AdminPostForm
  },
  data() {
    return {
      loadedPost: {
        author: 'Realdo Dias',
        title: 'My Updated Post',
        content: 'this an amazing post',
        thumbnail: 'https://s27389.pcdn.co/wp-content/uploads/2019/10/retail-innovation-changing-tech-consumer-employee-demands-1024x440.jpeg'
      }
    }
  }
}
</script>

<style scoped>
.admin-post-page {
  padding: 20px;
}

.update-form {
  padding-bottom: 10px;
}
</style>