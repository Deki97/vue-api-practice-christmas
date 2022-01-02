<template>
    <main>
        <div class="container">
            <div v-if="cards.length > 0" class="cards-list">
                <SingleCard v-for="(item, index) in cards" :key="index" :objectCard="item"/>
            </div>

            <Loader v-else />
        </div>
    </main>
</template>


<script>
import axios from 'axios';
import SingleCard from './SingleCard.vue';
import Loader from './Loader.vue';

export default {
    name: 'Main',
    components: {
        SingleCard,
        Loader
    },
    data: function() {
        return {
            cards: []
        };
    },
    created: function() {
        axios.get('https://api.sampleapis.com/cartoons/cartoons2D')
        .then((response) => {
            this.cards = response.data;
        });
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