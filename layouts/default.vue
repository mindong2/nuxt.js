<template>
    <!-- header, footer처럼 모든페이지 공통으로 들어가면 layout을 사용하면 편리하다 -->
    <div>
        <header>
            <h1 v-if = "this.isRoute">{{ $route.name }} 페이지</h1>
            <h1 v-else>error 페이지</h1>
            <NuxtLink to="/">홈페이지</NuxtLink>
            <NuxtLink to="/main">메인 페이지</NuxtLink>
            <NuxtLink to="/product">상품 페이지</NuxtLink>
        </header>
        <Nuxt />
    </div>
</template>

<script>
    export default {
        computed : {
            isRoute() {
                return this.$route.name;
            }
        }
    }
</script>

<style scoped>
    a {color: #00dc82; text-decoration: none;}
</style>
  