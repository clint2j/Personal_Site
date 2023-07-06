<script setup lang="ts">
    // interface linkInfo {
    //     name: string,
    //     url: string
    // }
    // const navBar = reactive<Array<linkInfo>>([
    //     {name: "Home", url: "/"},

    // ]);
    const router = useRouter();
    const currRoutes = computed(()=>router.getRoutes());
</script>
<template>
    <h1>Test123</h1>
    <NavItem v-for="route in currRoutes"
        :title="route.name"
        :url="route.path"
    />
</template>