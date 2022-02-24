<template>
    <div class="menu">
        <div class="item" id="Connect" @click="toggle">Connect</div>
        <div class="item">Control</div>
        <div class="item">View</div>
        <div class="item">Navigation</div>
        <div class="item">task</div>
    </div>
    <robotConnect :disabled="close" @click="toggle"/>
</template>
<script>
import robotConnect from '@/components/robotConnect.vue'
export default {
    name: 'robotMenu',
    components: {
        robotConnect,
    },
    data() {
        return {
            close: true
        }
    },
    methods:{
        toggle(){
            this.close = !this.close
        },
     
    }
}
</script>
<style scoped>
.menu {
    display: flex;
    position: fixed;
    bottom: 0;
    background-color: rgb(19, 77, 110);
    width: 100%;
    font-size: 0px;
    border-radius: 10px 10px 0px 0px;
    box-shadow: 0px -1px 10px 0.5px rgba(0, 0, 0, 0.8);
    color: wheat;
}

.item {
    width: 100%;
    padding: 12px 8px;
    font-size: 18px;
    text-align: center;
    cursor: pointer;
}

.item:hover {
    transition: .3s;
    background-color: rgb(235, 43, 36);
    color: rgb(5, 0, 0);
    border-radius: 5px;
}
</style>