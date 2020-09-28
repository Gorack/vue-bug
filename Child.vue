<template>
	<div>
		<p>Child component...</p>
	</div>
</template>

<script lang="ts">
    import {Component, Ref, Vue} from 'vue-property-decorator';

    @Component({
        name: 'Child'
    })
    export default class Child extends Vue {
        childMethod() {
            console.log('childMethod called');
        }
    }
</script>

<style scoped>

</style>
