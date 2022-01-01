<template>
    <header>
        <div class="logo">
            <img src="../assets/img/boing-logo.png" alt="Boing Logo">
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
    background-color: $primary-color;
    padding: 10px 30px;

    .logo {
        width: 80px;
    }
}
</style>