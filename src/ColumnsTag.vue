<script setup lang="ts">
import DtCore from 'datatables.net';
import DataTable, { Column } from 'datatables.net-vue3';
import Tag from './Tag.vue';

DataTable.use(DtCore);

function rowClick(data: any) {
	console.log('Tag clicked for row', data);
}
</script>

<template>
	<div>
		<h2>Column component: With a Child Component</h2>
		<p>
			This example demonstrates the <code>Column</code> component being used while its own child component to display in the table.
		</p>
		<DataTable class="display" ajax="/data.json">
			<Column title="Name" data="name" />
			<Column title="Position" data="position" />
			<Column title="Office" data="office" v-slot="props">
				<Tag
					:value="props.cellData"
					@click="rowClick(props.rowData)"
				></Tag>
			</Column>
			<Column title="Extn." data="extn" v-slot="props">
				<a :href="`tel:${props.cellData}`">{{props.cellData}}</a>
			</Column>
			<Column title="Start date" data="start_date" :render="DtCore.render.date()" />
			<Column title="Salary" data="salary" />
		</DataTable>
	</div>
</template>
