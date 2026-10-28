<script setup lang="ts">
import DtCore from 'datatables.net';
import DataTable, { Column } from 'datatables.net-vue3';

DataTable.use(DtCore);
</script>

<template>
	<div>
		<h2>Column component: attributes only</h2>
		<p>
			This example demonstrates the <code>Column</code> component being used in the <code>DataTable</code> with title and data properties.
		</p>
		<DataTable class="display" ajax="/data.json">
			<Column title="Name" data="name" />
			<Column title="Position" data="position" />
			<Column title="Office" data="office" />
			<Column title="Extn." data="extn" />
			<Column title="Start date" data="start_date" />
			<Column title="Salary" data="salary" />
		</DataTable>
	</div>
</template>
