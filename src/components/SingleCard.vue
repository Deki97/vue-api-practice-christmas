<template>
    <div class="card">
        <div class="card-image">
            <img src="https://nick.mtvnimages.com/uri/mgid:arc:content:nick.com:9cd2df6e-63c7-43da-8bde-8d77af9169c7?quality=0.7" alt="Spongebob Image">
        </div>

        <div class="card-title">
            Spongebob Squarepants
        </div>

        <div class="card-year">
            Year: 1999
        </div>

        <div class="card-episodes">
            Episodes: 272
        </div>

        <div class="card-creator">
            Creator: Stephen Hillenburg
        </div>
    </div>
</template>


<script>
export default {
    name: 'SingleCard'
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
    &-creator {
        color: $primary-color;
        font-size: 14px;
        font-weight: bold;
    }
}
</style>