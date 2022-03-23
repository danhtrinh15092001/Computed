<template>
    <div class="hello">
        <div v-for="book in Story" :key="book.id">
            {{ book.title }}
        </div>
    </div>
</template>

<script>
export default {
    name: "App",
    data() {
        return {
            animes: [
                { id: "1", title: "Naruto", author: "Danh", isFav: true },
                { id: "2", title: "Onepiece", author: "Dien", isFav: false },
                { id: "3", title: "DragonBall", author: "Duc", isFav: true },
            ],
        };
    },
    computed: {
        Story() {
            return this.animes.filter((anime) => anime.isFav);
        },
    },
};
</script>

<style>
#app {
    font-family: Avenir, Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    font-size: 24px;
    color: #2c3e50;
    margin-top: 60px;
}
</style>
