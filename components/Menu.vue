<template>
    <div class="menu">
        <div class='menu-select'>
            <Select/>
        </div>
        <div class='menu-items'>
            <MenuItem/>
            <MenuItem/>
            <MenuItem/>
            <MenuItem/>
            <MenuItem/>
            <MenuItem/>
            <MenuItem/>
            <MenuItem/>
            <MenuItem/>
        </div>
    </div>
    
</template>

<style lang="scss">
@import url('https://fonts.googleapis.com/css?family=Source+Sans+Pro');

.menu {
    display: inline-flex;
    flex-direction: column;
    margin: 32px 32px 0px 16px;
}

.menu-select {
    text-align: right;
    width: 100%;

    @media(max-width: 1094px) {
        text-align: left; 
    }
}

.menu-items {
   display: flex;
   flex-direction: row;
   flex-wrap: wrap;
   justify-content: space-between;
   
}

</style>
