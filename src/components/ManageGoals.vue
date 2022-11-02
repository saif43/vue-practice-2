<template>
    <div>
        <h4>Manage Goals</h4>
        <input type="text" ref="goalInput">
        <button @click="setGoal">Set Goal</button>

        <ErrorAlert v-if="hasInputError">
            <h2>Input is invalid</h2>
            <p>Please enter few words...</p>
            <button @click="confirmError">Ok</button>
        </ErrorAlert>
        
        
    </div>
</template>
<script>
import ErrorAlert from './ErrorAlert.vue';

export default {
    name: 'ManageGoals',
    components: {
        ErrorAlert
    },
    data() {
        return {
            hasInputError: false
        }
    },
    methods: {
        setGoal(){
            const enterValue = this.$refs.goalInput.value;

            if(enterValue === ''){
                this.hasInputError = true;
            }
        },
        confirmError(){
            this.hasInputError = false;
        }
    }
}
</script>
<style lang="">
    
</style>