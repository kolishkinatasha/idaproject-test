<template>
    <div class='menu-item'>
        <div class='delete'>
            <img src="../static/delete.svg">
        </div>
        <img class='menu-item-img' src='../static/foto.png' alt='foto item'/>
        <div class='menu-content'>
            <h2 class='menu-item-title'>Наименование товара</h2>
            <p class='menu-item-descr'>Довольно-таки интересное описание товара в несколько строк. Довольно-таки интересное описание товара в несколько строк</p>
            <p class='menu-item-price'>10 000 руб.</p>
        </div>
    </div>
</template>

<style lang="scss">
@import url('https://fonts.googleapis.com/css?family=Source+Sans+Pro');

.menu-item {
    width: 332px;
    height: 423px;
    margin-bottom: 16px;
    position: relative;

    background: #FFFEFB;
    box-shadow: 0px 20px 30px rgba(0, 0, 0, 0.04), 0px 6px 10px rgba(0, 0, 0, 0.02);
    border-radius: 4px; 
}

.menu-item:hover .delete {
    opacity: 1;
}

.menu-content {
    padding: 16px 16px 24px 16px;
}

.delete {
    position: absolute;
    width: 32px;
    height: 32px;
    top: -8px;
    right: -8px;

    background: #FF8484;
    box-shadow: 0px 2px 4px rgba(0, 0, 0, 0.1);
    border-radius: 10px;
    opacity: 0;

    img {
        margin: 8px;
    }
}

.menu-item-img {
    width: 332px;
    height: 200px;
    border-radius: 4px 4px 0px 0px;
}

.menu-item-title {
    margin: 0;
    font-family: Source Sans Pro;
    font-style: normal;
    font-weight: 600;
    font-size: 20px;
    line-height: 25px;

    color: #3F3F3F;
}

.menu-item-descr {
    margin: 16px 0 32px 0;

    font-family: Source Sans Pro;
    font-style: normal;
    font-weight: normal;
    font-size: 16px;
    line-height: 20px;

    color: #3F3F3F;
}

.menu-item-price {
    margin: 0;
    padding: 0;

    font-family: Source Sans Pro;
    font-style: normal;
    font-weight: 600;
    font-size: 24px;
    line-height: 30px;

    color: #3F3F3F;
}
</style>
