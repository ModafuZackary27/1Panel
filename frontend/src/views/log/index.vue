<template>
    <div>
        <RouterButton :buttons="buttons" />
        <LayoutContent>
            <router-view></router-view>
        </LayoutContent>
    </div>
</template>

<script lang="ts" setup>
import i18n from '@/lang';
import LayoutContent from '@/layout/layout-content.vue';
import RouterButton from '@/components/router-button/index.vue';

const buttons = [
    {
        label: i18n.global.t('logs.operation'),
        path: '/logs/operation',
    },
    {
        label: i18n.global.t('logs.login'),
        path: '/logs/login',
    },
    {
        label: i18n.global.t('logs.system'),
        path: '/logs/system',
    },
    {
        label: i18n.global.t('ssh.loginLogs'),
        path: '/logs/ssh',
    },
];
</script>
