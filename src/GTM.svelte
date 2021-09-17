<script lang="ts">
    import Input from "./ui/Input.svelte";
    import Button from "./ui/Button.svelte";
    import { addToHead } from "./functions/addToHead";
    export let visible = false;

    let containerID = null;
    let isConfigured = false;

    const onSetClick = () => {
        isConfigured = true;


        const code = `(function(w,d,s,l,i){w[l]=w[l]||[];w[l].push({'gtm.start':
new Date().getTime(),event:'gtm.js'});var f=d.getElementsByTagName(s)[0],
j=d.createElement(s),dl=l!='dataLayer'?'&l='+l:'';j.async=true;j.src=
'https://www.googletagmanager.com/gtm.js?id='+i+dl;f.parentNode.insertBefore(j,f);
})(window,document,'script','dataLayer','${containerID}');`;
        eval(code);
    }

</script>

<div class:hidden={!visible}>
    <Input placeholder="GTM-XXXX" bind:value={containerID} />
    <Button on:click={onSetClick}>Set</Button>
</div>

<style>
    .hidden {
        display: none !important;
    }
</style>