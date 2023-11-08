<template>
    <a-card :style="{ width: '400px', margin: '0 auto' }">
      <h2 class="text-center mb-4">注册</h2>
      <a-form :model="form" @finish="handleFinish" layout="vertical">
        <a-form-item
          name="username"
          label="用户名"
        >
          <a-input v-model:value="form.username" placeholder="请输入用户名" />
        </a-form-item>
        <a-form-item
          name="email"
          label="邮箱"
        >
          <a-input v-model:value="form.email" placeholder="wetest@example.com" />
        </a-form-item>
        <a-form-item
          name="password"
          label="密码"
        >
          <a-input-password v-model:value="form.password" placeholder="请输入密码" />
        </a-form-item>
        <a-form-item>
          <a-space split>
            <a-button type="primary" html-type="submit">注册</a-button>
          </a-space>
        </a-form-item>
      </a-form>
    </a-card>
  </template>
  
  <script setup lang="ts">
  import { reactive } from 'vue';
  definePageMeta({
    layout: 'entry',
  })
  const form = reactive({
    username: '',
    email: '',
    password: '',
  });
  
  const handleFinish = (values: any) => {
    console.log('Form values:', values);
  };
  </script>
  
  <style>
  .text-center {
    text-align: center;
  }
  .mb-4 {
    margin-bottom: 1rem;
  }
  </style>