<script lang="ts">
    export let visible = false;
</script>

<div class:hidden={!visible}></div>

<style>
    .hidden {
        display: none !important;
    }
</style>