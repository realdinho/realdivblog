<template>
  <section class="post-list">
       <PostPreview 
        id="1" 
        title="Shortcuts in VUE" 
        previewText="This is my first post" 
        thumbnail="https://s27389.pcdn.co/wp-content/uploads/2019/10/retail-innovation-changing-tech-consumer-employee-demands-1024x440.jpeg" 
      />
      <PostPreview 
        id="2" 
        title="Tech is Awesome" 
        previewText="This is my second post" 
        thumbnail="https://s27389.pcdn.co/wp-content/uploads/2019/10/retail-innovation-changing-tech-consumer-employee-demands-1024x440.jpeg" 
      />
      <PostPreview 
        id="3" 
        title="VUE is cool but NUXT is better" 
        previewText="This is my third post" 
        thumbnail="https://s27389.pcdn.co/wp-content/uploads/2019/10/retail-innovation-changing-tech-consumer-employee-demands-1024x440.jpeg" 
      />
      <PostPreview 
        id="4" 
        title="Welcome to NUXT JS"
        previewText="This is my fourth post" 
        thumbnail="https://s27389.pcdn.co/wp-content/uploads/2019/10/retail-innovation-changing-tech-consumer-employee-demands-1024x440.jpeg" 
      />
    </section>
</template>

<script>
  import PostPreview from '@/components/Posts/PostPreview'

  export default {
    components: {
      PostPreview
    }
  }
</script>

<style scoped>
  .post-list {
    display: flex;
    padding: 20px;
    box-sizing: border-box;
    flex-wrap: wrap;
    align-items: center;
    justify-content: center;
  }
</style>