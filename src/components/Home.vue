<template>
    <div class="row">
        <div class="leftcolumn">
        <blog-post></blog-post>
        <blog-post></blog-post>
        <blog-post></blog-post>
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
  }
}
</script>
