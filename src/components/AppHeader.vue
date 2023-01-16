<script>
export default {
}
</script>
<template lang="">
    <header>
        <div class="header">
        <a href="#">
            <img class="logo" src="http://vignette1.wikia.nocookie.net/yugiohenespanol/images/a/aa/Yugioh_anime_logo.jpg/revision/latest?cb=20130310042737&path-prefix=es" alt="logo">
        </a>
        <h2>
            Yu-Gi-Oh Api
        </h2>
        </div>
    </header>
</template>
<style lang="scss">
    @use '../styles/partials/variables' as *; 
    @use '../styles/partials/mixins' as *; 
    .header{
        display: flex;
        flex-direction: row;
        align-items: center;
        .logo{
            width: 100px;
            margin: 20px;
        }
    }
</style>