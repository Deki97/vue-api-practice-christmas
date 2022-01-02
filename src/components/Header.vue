<template>
    <header>
        <div class="logo">
            <img src="../assets/img/boing-logo.png" alt="Boing Logo">
        </div>

        <div class="title">
            <h1>Cartoons API</h1>
        </div>
    </header>
</template>


<script>
export default {
    name: 'Header'
}
</script>


<style lang="scss" scoped>
@import '../style/variables.scss';

header {
    display: flex;
    align-items: center;
    justify-content: space-between;
    background-color: $primary-color;
    padding: 10px 30px;

    .logo {
        width: 80px;
    }

    .title {
        color: $secondary-color;
    }
}
</style>