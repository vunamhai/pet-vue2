<template>
<HomePage/>
    <ContentUser/>
      <OurBlogUser/>
  <FooterUser/>
   <HeaderUser/>
</template>

<script>

// @ is an alias to /src
import HeaderUser from '@/components/HeaderUser.vue'
import HomePage from '@/components/HomePage.vue'
import ContentUser from '@/components/ContentUser.vue'
import OurBlogUser from '@/components/OurBlogUser.vue'
import FooterUser from '@/components/FooterUser.vue'
export default {
  name: 'HomeView',
  components: {
    HeaderUser,
    HomePage,
    ContentUser,
    OurBlogUser,
    FooterUser,
    
  }
}
</script>
