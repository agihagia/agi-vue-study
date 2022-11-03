<script setup>
import { NLayoutSider, NMenu } from 'naive-ui';
import {h} from 'vue';
import { RouterLink } from 'vue-router';
const menus=[
    {title: 'Home', to:'/'},
    {title: 'Pegawai', to:'/pegawai'},
    {title: 'Absen', to:'/absen'},
]

const menuOptions = menus.map((menu) => {
    return{
        label : () => h(
            RouterLink,
            {to: menu.to},
            {default: () => menu.title}
        ),
        key: menu.to,
        icon:null
    }
})

</script>

<template>
    <n-layout-sider bordered show-trigger="arrow-circle">
        <NMenu :options="menuOptions" />
      </n-layout-sider>
</template>