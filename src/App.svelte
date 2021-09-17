<script lang="ts">
	import GTM from "./GTM.svelte";
    import GTag from "./GTag.svelte";
    import Button from "./ui/Button.svelte";

    let name = 'world';
    let selectedCounter = 'gtm';
</script>

<div>
    <Button on:click={() => selectedCounter = 'gtm'}>GTM</Button>
    <Button on:click={() => selectedCounter = 'gtag'}>Google Tag</Button>
</div>
<GTM visible={selectedCounter === 'gtm'} />
<GTag visible={selectedCounter === 'gtag'} />

