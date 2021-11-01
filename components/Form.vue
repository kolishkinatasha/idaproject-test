<template>
    <form
    class='sidebar-wrapper'>        
        <div class='sidebar-item'>
            <label class='sidebar-label'>Наименование товара</label>
            <div class='label__important'></div>
            <input class='sidebar-input' 
            type='text' 
            placeholder='Введите наименование товара'/>
        </div>
        <div class='sidebar-item'>
            <label  class='sidebar-label'>Описание товара</label>
            <textarea class='sidebar-input sidebar-input__long' placeholder='Введите описание товара'/>
        </div>
        <div class='sidebar-item'>
            <label  class='sidebar-label'>Ссылка на изображение товара</label>
            <input class='sidebar-input' 
            placeholder='Введите ссылку'/>
        </div>
        <div class='sidebar-item'>
            <label  class='sidebar-label'>Цена товара</label>
            <div class='label__important'></div>
            <input class='sidebar-input' placeholder='Введите цену'/>
        </div>
        
        <button type="submit" class='sidebar-btn'>Добавить товар</button>
    </form>
</template>

<script>
export default {

};
</script>


<style lang='scss'>
@import url('https://fonts.googleapis.com/css?family=Source+Sans+Pro');

.sidebar-wrapper {
    width: 284px;

    padding: 24px;
    margin-top: 16px;
    margin-left: 32px;
    text-align: center;

    background: #FFFEFB;
    box-shadow: 0px 20px 30px rgba(0, 0, 0, 0.04), 0px 6px 10px rgba(0, 0, 0, 0.02);
    border-radius: 4px;
}

.sidebar-item {
    display: flex;
    flex-wrap: wrap;
    padding: 0;
    margin: 0 auto;
}

.sidebar-label {
    font-family: Source Sans Pro;
    font-style: normal;
    font-weight: normal;
    font-size: 10px;
    line-height: 13px;
    letter-spacing: -0.02em;
    color: #49485E;
}

.label__important {
    width: 4px;
    height: 4px;
    left: 151px;
    top: 107px;

    background: #FF8484;
    border-radius: 50%;
}

.sidebar-input {
    width: 100%;
    height: 34px;
    border: none;
    padding-left: 16px;
    margin: 4px 0px 16px 0px;

    background: #FFFEFB;
    box-shadow: 0px 2px 5px rgba(0, 0, 0, 0.1);
    border-radius: 4px;

    ::placeholder {
    font-family: Source Sans Pro;
    font-style: normal;
    font-weight: normal;
    font-size: 12px;
    line-height: 15px;

    margin-top: 10px;

    text-align: left;
    color: #B4B4B4;
}
}

.sidebar-input__long {
    height: 108px;
    resize: none;
    padding-top: 10px;
}

.sidebar-btn{
    width: 100%;
    height: 36px;
    border: none;

    background: #EEEEEE;
    border-radius: 10px;

    font-family: Inter;
    font-style: normal;
    font-weight: 600;
    font-size: 12px;
    line-height: 15px;
    text-align: center;
    letter-spacing: -0.02em;
    color: #B4B4B4;
}
</style>
