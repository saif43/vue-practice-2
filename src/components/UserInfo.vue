<template>
<BaseSlot>
    <template v-slot:header>
        <h3>{{ fullName }}</h3>
        <base-badge :type="role" :caption="role.toUpperCase()"></base-badge>
    </template>
    <template v-slot:default>
        <p>{{ infoText }}</p>
    </template>
</BaseSlot>
</template>

<script>
import BaseBadge from './BaseBadge.vue';
import BaseSlot from './BaseSlot.vue';

export default {
    name: 'UserInfo',
    props: ['fullName', 'infoText', 'role'],
    components: {
        BaseSlot,
        BaseBadge
    }
};
</script>

<style lang="scss" scoped>

</style>
