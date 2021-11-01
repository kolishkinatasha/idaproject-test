<template>
    <div class="main">
        <Sidebar/>
        <Menu/>
    </div>   
</template>

<style lang="scss">
div {
    margin: 0;
    padding: 0;
}

.main {
    display: flex;
    @media(max-width: 722px) {
        flex-wrap: wrap;
        flex-direction: column;
    }
}
</style>

<script>
export default {}
</script>
