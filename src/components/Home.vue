<template>
    <div class="row">
        <div class="leftcolumn">
          <blog-post 
            v-for="article in articles" 
            :key="article" 
            :article="article">
          </blog-post>
        </div>
        <div class="rightcolumn">
        <about></about>
        <div class="card">
            <h3>Popular Post</h3>
            <div class="fakeimg"><p>Image</p></div>
            <div class="fakeimg"><p>Image</p></div>
            <div class="fakeimg"><p>Image</p></div>
        </div>
        <div class="card">
            <h3>Follow Me</h3>
            <p>Some text..</p>
        </div>
        </div>
    </div>
</template>    
<script>
import About from "./About.vue"
import BlogPost from "./BlogPost.vue"

export default {
  components: {
    About, BlogPost
  },
  data: function() {
    return {
      articles: []
    }
  },
  mounted: function() {
    for (let i=0;i<10;i++) {
      this.articles.push(
        { 
          title:"Title "+i, 
          subtitle:"El subtitulo "+i, 
          body: i+"Lorem ipsum slkdjfsdkfjsdfshfd hs dfsdhfsdfh " 
        });
    }
  }
}
</script>
