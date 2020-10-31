<template>
    <div class="container">
        <label for="">全屏布局</label>
        <div class="all">
            <header></header>
            <main></main>
            <footer></footer>
        </div>
    </div>

    <div class="container">
        <div class="flex">
            <header></header>
            <main></main>
            <footer></footer>
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
    width: 100vw;
    height: 100vh;
    display: flex;
    .all {
        position: relative;
        width: 400px;
        height: 100%;
        header,
        footer,
        main {
            position: absolute;
            left: 0;
            right: 0;
            display: flex;
            align-items: center;
            justify-content: center;
        }
        header {
            top: 0;
            height: 60px;
            background-color: #f66;
        }
        footer {
            bottom: 0;
            height: 100px;
            background-color: #66f;
        }
        main {
            top: 50px;
            bottom: 100px;
            background-color: #3c9;
        }
    }
    .flex {
        width: 50vw;
        height: 100vh;
        display: flex;
        align-items: center;
        flex-direction: column;
        header,
        main,
        footer {
            width: 100%;
        }
        header {
            height: 50px;
            background-color: #f66;
        }
        main {
            flex: 1;
            background-color: #66f;
        }
        footer {
            height: 100px;
            background-color: #3cf;
        }
    }
}
</style>
