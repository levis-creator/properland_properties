<script lang="ts">
	interface SectHeader {
		no: number;
		section_title: string;
		title: string;
		position?: 'center' | 'left' | 'right';
	}
	export let head: SectHeader;
</script>

<div class="space-y-7 px-4">
	<h3
		class="uppercase space-x-5 text-blue-900 w-fit border-x-2 border-x-blue-900 px-3 tracking-[0.3em]"
	>
		<span class="text-yellow-300">{head.no}</span>
		{head.section_title}
	</h3>
	<h2 class="font-bold text-3xl text-blue-900">{head.title}</h2>
</div>
