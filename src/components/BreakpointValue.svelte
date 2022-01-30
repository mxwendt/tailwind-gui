<script>
	export let name;
	export let width;

	let colspan1 = 0;
	let colspan2 = 12;

	if (width) {
		colspan1 = width / 128;
		colspan2 = 12 - colspan1;
	}
</script>

<tr>
	<td>{name}</td>
	<td colspan={colspan1}>
		<div class="bg-blue-200 h-1 w-full" />
	</td>
	<td colspan={colspan2} />
</tr>
