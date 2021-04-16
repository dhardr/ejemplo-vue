<template>
    <div class="card">
        <h2>{{article.title}}</h2>
        <h5>{{article.subtitle}}, Dec 7, 2017</h5>
        <p>{{article.body}}</p>
    </div>
</template>
<script>
export default {
    props: ["article"],
}
</script>