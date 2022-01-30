<script>
	import BreakpointValue from './BreakpointValue.svelte';
</script>

<table class="w-full">
	<thead>
		<tr>
			<td />
			<td>0</td>
			<td>128</td>
			<td>256</td>
			<td>384</td>
			<td>512</td>
			<td class="font-bold">640</td>
			<td class="font-bold">768</td>
			<td>896</td>
			<td class="font-bold">1024</td>
			<td>1152</td>
			<td class="font-bold">1280</td>
			<td>1408</td>
			<td class="font-bold">1536</td>
		</tr>
	</thead>
	<tbody>
		<BreakpointValue name="sm" width="640" />
		<BreakpointValue name="md" width="768" />
		<BreakpointValue name="lg" width="1024" />
		<BreakpointValue name="xl" width="1280" />
		<BreakpointValue name="2xl" width="1536" />
	</tbody>
</table>
