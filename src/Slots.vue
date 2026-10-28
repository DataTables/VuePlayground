<script setup lang="ts">
import DtCore from 'datatables.net';
import DataTable from 'datatables.net-vue3';
import Tag from './Tag.vue';

DataTable.use(DtCore);

const columns = [
	{data: 'name'},
	{data: 'position'},
	{data: 'office'},
	{data: 'extn'},
	{data: 'start_date'},
	{data: 'salary'}
];

function rowClick(data: any) {
	console.log('Tag clicked for row', data);
}
</script>

<template>
	<div>
		<h2>Vue Slots</h2>
		<p>
			This example demonstrates <code>DataTable</code> being used with a Vue component in a column through automatic slots. Here a column's data is displayed by another Vue component.
		</p>
		<DataTable class="display" ajax="/data.json" :columns="columns">
			<thead>
				<tr>
					<th>Name</th>
					<th>Position</th>
					<th>Office</th>
					<th>Age</th>
					<th>Start date</th>
					<th>Salary</th>
				</tr>
			</thead>
			<tfoot>
				<tr>
					<th>Name</th>
					<th>Position</th>
					<th>Office</th>
					<th>Age</th>
					<th>Start date</th>
					<th>Salary</th>
				</tr>
			</tfoot>
			<template #column-2="props">
				<Tag
					:value="props.cellData"
					@click="rowClick(props.rowData)"
				></Tag>
			</template>
		</DataTable>
	</div>
</template>
