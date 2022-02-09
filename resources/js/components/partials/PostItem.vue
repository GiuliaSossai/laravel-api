<template>
    <div class="item">
        <h4>{{ post.title }}</h4>
        <small>{{ post.created_at }}</small>
        <p>{{ post.content }}</p>
    </div>
</template>

<script>
export default {
    name: 'Post',

    props: {
        'post': Object
    }
}
</script>

<style lang="scss" scoped>
    .item {
        padding: 20px 0;
    }

</style>