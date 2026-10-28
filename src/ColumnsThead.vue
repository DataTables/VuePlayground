<script setup lang="ts">
import DtCore from 'datatables.net';
import DataTable, { Column } from 'datatables.net-vue3';

DataTable.use(DtCore);
</script>

<template>
	<div>
		<h2>Column component: with thead</h2>
		<p>
			This example demonstrates the <code>Column</code> component and <code>thead</code> being used together.
		</p>
		<DataTable class="display" ajax="/data.json">
			<thead>
				<tr>
					<th>Name</th>
					<th>Position</th>
					<th></th>
					<th>Start date</th>
					<th>Salary</th>
				</tr>
			</thead>
			<Column data="name" />
			<Column data="position" />
			<Column data="office" title="Office (title)" />
			<Column data="start_date" />
			<Column data="salary" />
		</DataTable>
	</div>
</template>
