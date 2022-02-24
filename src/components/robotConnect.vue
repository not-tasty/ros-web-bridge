<template>
    <div class="connect" v-if="disabled">
            <label for="RobotType">RobotType:</label>
            <input type="text">
            <label for="IP">IP:</label>
            <input type="text">
            <label for="Port">Port:</label>
            <input type="text">
        </div>
</template>

<script>
export default {
    name: 'robotConnect',
    props:{
        disabled: Boolean
    },
}
</script>
<style scoped>
.connect{
            width: 280px;
            height: 30%;
            display: flex;
            flex-wrap: wrap;
            padding: 10px;
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            margin: auto;
            backdrop-filter: blur(2px);
            border: 1px solid black;
            box-shadow: 0px 0px 40px black;
        }
        .connect > label{
            color: wheat;
        }
        .connect > input{
            width: 100%;
            margin: 6px 0px;
            font-size: 16px;
        }
</style>