<template>
	<div>
		<p>Parent</p>
		<Child ref="child"></Child>
	</div>
</template>

<script lang="ts">
    import {Component, Ref, Vue} from 'vue-property-decorator';
    import Child from './Child.vue';

    @Component({
        name: 'Parent',
	    components: {Child}
    })
    export default class Parent extends Vue {
        @Ref('child') readonly child: Child;

        mounted() {
            this.child.childMethod();
        }
    }
</script>

<style scoped>

</style>
