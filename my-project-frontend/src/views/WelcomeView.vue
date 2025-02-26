<script setup>

</script>

<template>
    <div style="width: 100vw;height: 100vh;overflow: hidden;display: flex">
        <div style="flex: 1;background-color: black">
            <el-image style="width: 100%;height: 100%;" fit="cover"
                      src="https://img2.baidu.com/it/u=1470164115,883139116&fm=253&fmt=auto?w=1280&h=800"/>
        </div>
        <div class="welcome-title">
            <div style="font-size: 30px;font-weight: bold">欢迎来到我们的学习平台</div>
            <div style="margin-top: 10px">在这里你们可以学习如何使用Java,如何搭建网站,并且彼此之间密切交流</div>
        </div>
        <div class="right-card">
            <router-view v-slot="{ Component }">
                <transition name="el-fade-in-linear" mode="out-in">
                    <component :is="Component"/>
                </transition>
            </router-view>
        </div>
    </div>
</template>

<style scoped>
.welcome-title {
    position: absolute;
    bottom: 30px;
    left: 30px;
    color: white;
    text-shadow: 0 0 10px;
}

.right-card {
    width: 400px;
    z-index: 1;
    background-color: var(--el-bg-color);
}
</style>