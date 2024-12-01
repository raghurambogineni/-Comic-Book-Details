<template>
    <div v-for="(book, index) of bookList" :key="book.comicBook_title">
        <!-- Send color by matching index -->
        <ComicBook :book = book :color="colors[index % colors.length]" />
    </div>
</template>

<script>
    import ComicBook from "./ComicBook.vue";

    export default{
        name:"ComicBookCatalog",
        components:{
           ComicBook
        },
        props:{
            bookList: Array
        },
        data() {
        return {
            colors: ["#ff746c", "#4781cb", "#8e6903", "#49636c", "#f4c445"]
        };
        }
    }
</script>

<style scoped>
</style>