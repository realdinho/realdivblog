<template>
  <div class="admin-page">
    <section class="new-post">
      <AdminPostForm />
    </section>
  </div>
</template>

<script>
import AdminPostForm from '@/components/Admin/AdminPostForm' 

export default {
  components: {
    AdminPostForm
  }
}
</script>

<style scoped>
.admin-page {
  padding: 20px;
}

.new-post {
  padding-bottom: 10px;
}

.existing-posts h1 {
  text-align: center;
}
</style>