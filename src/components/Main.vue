<template>
    <main>
        <div class="container">
            <div class="cards-list">
                <SingleCard />
            </div>
        </div>
    </main>
</template>


<script>
import SingleCard from './SingleCard.vue'

export default {
    name: 'Main',
    components: {
        SingleCard
    }
}
</script>


<style lang="scss" scoped>
main {
    padding: 50px 0;
    .container {
        .cards-list {
            display: flex;
            flex-wrap: wrap;
        }
    }
}
</style>