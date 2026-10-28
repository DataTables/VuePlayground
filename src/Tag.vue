<template>
	<div class="tag">
		<div class="tag-inner">
			{{ props.value }}
		</div>
	</div>
</template>

<script setup lang="ts">
import { onMounted } from 'vue';

const props = defineProps<{
	value: string | null;
}>();

onMounted(() => {
	// console.log('Tag component mounted');
	// console.log(props.value);
});
</script>

<style scoped>
.tag {
	display: inline-block;
}

.tag-inner {
	display: inline-block;
	padding: 0.25em 0.6em;
	font-size: 100%;
	font-weight: 700;
	line-height: 1;
	text-align: center;
	white-space: nowrap;
	vertical-align: baseline;
	border-radius: 0.25rem;
	background-color: #4caf7d;
	color: #ffffff;
	letter-spacing: 0.05em;
}
</style>
