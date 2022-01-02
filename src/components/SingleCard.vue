<template>
    <div class="card">
        <div class="card-image">
            <img :src="objectCard.image" :alt="objectCard.title">
        </div>

        <div class="card-title">
            {{ objectCard.title }}
        </div>

        <div class="card-year">
            Year: {{ objectCard.year }}
        </div>

        <div class="card-episodes">
            Episodes: {{ objectCard.episodes }}
        </div>

        <div class="card-minutes">
            Minutes: {{ objectCard.runtime_in_minutes }}
        </div>
    </div>
</template>


<script>
export default {
    name: 'SingleCard',
    props: {
        objectCard: Object
    }
}
</script>


<style lang="scss" scoped>
@import '../style/variables.scss';

.card {
    width: calc((100% / 5) - 20px);
    margin: 15px 10px;
    

    &-image {
        img {
            height: 250px;
            width: 100%;
            object-fit: cover;
            cursor: pointer;
        }
    }

    &-title {
        text-transform: uppercase;
        font-weight: bold;
        font-size: 14px;
        color: $secondary-color;
        cursor: pointer;
    }

    &-year,
    &-episodes,
    &-minutes {
        color: $primary-color;
        font-size: 14px;
        font-weight: bold;
    }
}
</style>