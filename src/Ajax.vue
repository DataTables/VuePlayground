<script setup lang="ts">
import DtCore from 'datatables.net';
import DataTable from 'datatables.net-vue3';

DataTable.use(DtCore);

const columns = [
	{data: 'name'},
	{data: 'position'},
	{data: 'office'},
	{data: 'extn'},
	{data: 'start_date'},
	{data: 'salary'}
];
</script>

<template>
	<div>
		<h2>Ajax sourced data</h2>
		<p>
			This example demonstrates <code>DataTable</code> being populated by Ajax sourced JSON data.
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
		</DataTable>
	</div>
</template>
