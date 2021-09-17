<script lang="ts">
    export let placeholder = ''
    export let value = null;
</script>
<input type="text" on:change placeholder={placeholder} bind:value={value}>