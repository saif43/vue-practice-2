<template>
<div>
    <TheHeader />
    <button @click="setSelectedComponent('ActiveGoals')">Active</button>
    <button @click="setSelectedComponent('ManageGoals')">Manage</button>
    <component :is="selectedComponent"></component>
</div>
</template>

<script>
import ActiveGoals from './components/ActiveGoals.vue';
import ManageGoals from './components/ManageGoals.vue';
import TheHeader from './components/TheHeader.vue';

export default {
    components: {
        TheHeader,
        ActiveGoals,
        ManageGoals,
    },
    data() {
        return {
            selectedComponent: "ActiveGoals"
        };
    },
    methods: {
        setSelectedComponent(cmp){
            this.selectedComponent = cmp;
        }
    }
};
</script>

<style lang="scss">
html {
    font-family: sans-serif;
}

body {
    margin: 0;
}
</style>
