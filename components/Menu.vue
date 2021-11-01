<template>
    <div class="menu">
        <div class='menu-select'>
            <Select/>
        </div>
        <div class='menu-items'>
            <MenuItem v-for="item in items" :key="item.id" :item="item"/>
        </div>
    </div>
    
</template>

<script>
import {data} from '../static/data';

export default {
    data: function() {
        return {
            items: data
        }   
    },
    methods: {},
    mounted() {
        console.log(this.items)
    },
}
</script>


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
