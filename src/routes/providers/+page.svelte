<div class="mx-auto max-w-screen-xl">
	<div class="text-xl breadcrumbs mb-4">
		<ul>
			<li><a href="..">UnUniFi KYC</a></li>
			<li>KYC Providers</li>
		</ul>
	</div>

	<script lang="ts">
		import { config } from '../../models/config';
		import { KycQueryClient } from '../../models/Kyc.client';
		import type { Provider } from '../../models/Kyc.types';
		import { CosmWasmClient } from '@cosmjs/cosmwasm-stargate';

		export let providers: Promise<Provider[]>;

		(async () => {
			const wasmClient = await CosmWasmClient.connect(config.endpoint);
			const client = new KycQueryClient(wasmClient, config.contractAddress);

			providers = client.providers();
		})();
	</script>

	<div class="flex flex-col gap-4">
		{#await providers}
			<div class="loading loading-ring loading-xl" />
		{:then providers}
			{#if providers.length === 0}
				<p>No providers found</p>
			{/if}
			{#each providers as provider}
				<div class="card bg-base-200 shadow-xl">
					<div class="card-body">
						<h2 class="card-title">
							{provider.name}
						</h2>
						<p>
							{provider.details}
						</p>
						<div class="overflow-x-auto">
							<table class="table">
								<tbody>
									<tr>
										<th>Address</th>
										<td>{provider.address}</td>
									</tr>
									<tr>
										<th>Security Contact</th>
										<td>{provider.security_contact}</td>
									</tr>
									<tr>
										<th>Website</th>
										<td>{provider.website}</td>
									</tr>
								</tbody>
							</table>
						</div>
					</div>
				</div>
			{/each}
		{/await}
	</div>
</div>
