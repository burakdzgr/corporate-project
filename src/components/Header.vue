<template>
    <header class="header border-b" >
        <div class="container mx-auto">
            <div class="header-items flex items-center justify-between">
                <div class="header-logo">
                    <router-link to="/">
                        <img src="@/assets/logo.png" alt="">
                    </router-link>
                </div>
                <nav class="header-">
                    <ul class="flex items-center">
                        <li v-for="(menu, key) in menus" :key="key" >
                            <router-link :to="{name: menu.url}" class="font-bold text-xl text-black px-4">{{menu.title}}</router-link>
                        </li>
                    </ul>
                </nav>
            </div>
        </div>
    </header >
</template>

<script>
export default {
    data() {
        return {
            menus : [
                {url:'Home',title: 'Home'},
                {url:'About',title: 'About'},
            ]
        }
    }
}
</script>

<style scoped>
.header{
    box-shadow:
      0 1px 1px hsl(0deg 0% 0% / 0.075),
      0 2px 2px hsl(0deg 0% 0% / 0.075),
      0 4px 4px hsl(0deg 0% 0% / 0.075),
      0 8px 8px hsl(0deg 0% 0% / 0.075),
      0 16px 16px hsl(0deg 0% 0% / 0.075)
    ;

}
.header-logo img{
    width: 100px;
    height: 100%;
    object-fit: cover;
}
</style>