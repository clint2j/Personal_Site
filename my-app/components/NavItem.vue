<script setup lang="ts">
    const route = useRoute();
    const router = useRouter();
    const props = defineProps({
        title:String,
        url:String
    })
    const goHere = () => {
        router.push({path: props.url??"/"});
    }
    const isHere = computed(() => {
        return route.name == props.title;
    })
</script>


<template>
    <button @click="goHere" :class="'pr-5 ' + (isHere ? 'border-2 border-rose-500' : '')">{{ props.title!="index" ? props.title : "Home" }}</button>
</template>