<template>
<div>
    <TheHeader />
    <BadgeList />
    <UserInfo :full-name="activeUser.name" :info-text="activeUser.description" :role="activeUser.role" />
    <CourseGoals>
        <template v-slot:default="slotProps">
            <h4>{{slotProps.item}}</h4>
        </template>
    </CourseGoals>
    <CourseGoals>
        <template v-slot:default="slotProps">
            <p>{{slotProps.item}}</p>
        </template>
    </CourseGoals>
</div>
</template>

<script>
import BadgeList from './components/BadgeList.vue';
import CourseGoals from './components/CourseGoals.vue';
import TheHeader from './components/TheHeader.vue';
import UserInfo from './components/UserInfo.vue';

export default {
    components: {
        TheHeader,
        BadgeList,
        UserInfo,
        CourseGoals
    },
    data() {
        return {
            activeUser: {
                name: 'Maximilian Schwarzmüller',
                description: 'Site owner and admin',
                role: 'admin',
            },
        };
    },
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
