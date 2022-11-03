<script setup>
import { RouterLink, RouterView } from 'vue-router'
import { NSpace, 
NButton, 
NLayout, 
NLayoutContent } from 'naive-ui';
import Header from './layouts/Header.vue';
import Footer from './layouts/Footer.vue';
import Sidebar from './layouts/Sidebar.vue';
</script>

<template>
<!-- <NSpace vertical size="large"> -->
  <n-layout has-sider>
      <Sidebar/>
      <n-layout style="min-height: 100vh;">
        <Header />
        <n-layout-content content-style="padding: 24px;">
          <RouterView />
        </n-layout-content>
        <Footer />
      </n-layout>
    </n-layout>
<!-- </NSpace> -->


  <!--header>
    <img alt="Vue logo" class="logo" src="@/assets/logo.svg" width="125" height="125" />

    <div class="wrapper">
      <nav>
        <RouterLink to="/">Home</RouterLink>
      </nav>
    </div>
  </!--header>

  <NSpace>
    <NButton>Ini Sebuah Data</NButton>
    <NButton type="primary">
      Primary
    </NButton>
  </NSpace>

  <RouterView /-->
</template>
