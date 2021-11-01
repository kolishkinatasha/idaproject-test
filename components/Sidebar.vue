<template>
    <div class='wrapper'>
        <h1 class='sidebar-title'>Добавление товара</h1>
        <Form/>
    </div>
</template>

<style lang="scss">
@import url('https://fonts.googleapis.com/css?family=Source+Sans+Pro');

.sidebar-title {
    width: 247px;
    height: 35px;

    margin: 32px 0px 16px 32px;

    font-family: Source Sans Pro;
    font-style: normal;
    font-weight: 600;
    font-size: 28px;
    line-height: 35px;

    color: #3F3F3F;
}

@media(max-width: 722px) {
   .wrapper {
      margin-left: -16px;
   } 
}


</style>
