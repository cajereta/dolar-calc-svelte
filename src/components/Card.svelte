<script>
	import { Skeleton } from 'flowbite-svelte';
	import { fade } from 'svelte/transition';
	$: ({ ...restProps } = $$props);
	$: values = Object.values(restProps);
	$: list = [
		{
			id: 1,
			value: values[0],
			label: 'Impuesto PAÍS(30%)',
		},
		{
			id: 2,
			value: values[1],
			label: 'Imp. a las ganancias(45%)',
		},
		{
			id: 3,
			value: values[2],
			label: 'Total',
		},
	];
</script>

{#if !values[3] || values[3] == 0}
	<Skeleton size="xxl" class="my-8" />
{:else}
	<div
		class="flow-root my-4 break-normal"
		transition:fade={{ delay: 250, duration: 300 }}
	>
		<ul role="list" class="divide-y divide-gray-200 dark:divide-gray-700">
			{#each list as item}
				<li class="py-3 sm:py-4">
					<div class="flex items-center space-x-4">
						<div class="flex-shrink-0"></div>
						<div class="flex-1 min-w-0">
							<p
								class="text-sm text-left font-medium text-gray-900 truncate dark:text-white"
							>
								{item.label}
							</p>
						</div>
						<div
							class="inline-flex items-center text-base font-semibold text-gray-900 dark:text-white"
						>
							{#if item.value != 0}
								{new Intl.NumberFormat('es-AR', {
									style: 'currency',
									currency: 'ARS',
								}).format(item.value)}
							{:else}
								<p class="mr-2">-</p>
							{/if}
						</div>
					</div>
				</li>
			{/each}
			<li class="py-3 sm:py-4">
				<div class="flex items-center space-x-4">
					<div class="flex-shrink-0"></div>
					<div class="flex-1 min-w-0">
						<p
							class="text-sm text-left font-bold text-gray-900 truncate dark:text-white"
						>
							COTIZACIÓN DOLAR OFICIAL
						</p>
					</div>
					<div
						class="inline-flex items-center text-base font-semibold text-gray-900 dark:text-white"
					>
						{#if values[3] != 0}
							1 USD = {new Intl.NumberFormat('es-AR', {
								style: 'currency',
								currency: 'ARS',
							}).format(values[3])}
						{:else}
							<p class="mr-2">-</p>
						{/if}
					</div>
				</div>
			</li>
		</ul>
	</div>
{/if}
