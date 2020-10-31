<template>
    <div class="container">
        <h4>居中对齐</h4>
        <div class="flex box">
            <div class="color"></div>
        </div>
        <div class="flex1 box">
            <div class="color"></div>
        </div>
        <div class="grid box">
            <div class="color"></div>
        </div>

        <div class="transform-position box">
            <div class="color"></div>
        </div>
    </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue';

export default defineComponent({
    setup() {
        return {};
    },
});
</script>

<style lang="scss" scoped>
.container {
    display: grid;
    grid-template-rows: repeat(auto-fill, 300px);
    grid-template-columns: repeat(auto-fill, 300px);

    .box {
        position: relative;
        width: 300px;
        height: 300px;
        margin-bottom: 10px;
        background-color: rgb(167, 219, 25);
        .color {
            width: 100px;
            height: 100px;
            background-color: rgb(22, 223, 39);
        }
    }

    .flex {
        display: flex;
        align-items: center;
        justify-content: center;
        &::before {
            position: absolute;
            left: 10px;
            top: 10px;
            font-size: 20px;
            content: 'flex';
            color: #fff;
        }
    }

    .flex1 {
        display: flex;
        .color {
            margin: auto;
        }
        &::before {
            position: absolute;
            left: 10px;
            top: 10px;
            font-size: 20px;
            content: 'flex margin';
            color: #fff;
        }
    }

    .grid {
        display: grid;
        place-items: center;
        &::before {
            position: absolute;
            left: 10px;
            top: 10px;
            content: 'grid';
            color: #fff;
        }
    }

    .transform-position {
        &::before {
            position: absolute;
            left: 10px;
            top: 10px;
            color: #fff;
            content: 'transform-position';
        }
        .color {
            position: absolute;
            left: 50%;
            top: 50%;
            transform: translate(-50%, -50%);
        }
    }
}
</style>
