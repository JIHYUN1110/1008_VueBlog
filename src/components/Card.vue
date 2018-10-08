<template>
    <div>
        <b-card header="( ⸝⸝•ᴗ•⸝⸝ )੭⁾⁾"
                header-text-variant="white"
                header-tag="header"
                header-bg-variant="info"
                v-bind:footer="created"
                footer-tag="footer"
                footer-bg-variant="light"
                footer-border-variant="dark"
                v-bind:title="title"
                style="max-width: 70rem; margin-left: 2rem;"
        >
            <p class="card-text">{{ body }}</p>
            <div>
                <strong>댓글</strong>
                <comment 
                v-for="(comment,i) in comments"
                :key="comment.id"
                :index="i + 1"
                :body="comment.body"></comment>
            </div>
        </b-card>
    </div>
</template>



<script>
    import Comment from "./Comment.vue";
    export default {
        props: ['title','body','created','comments'],
        components :{
            Comment
        }
    }
</script>

<style>
</style>