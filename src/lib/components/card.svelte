<script lang="ts">
    export let img
    export let name
</script>
<div class="border-r border-b border-l border-gray-400 rounded shadow-md">
    <img src={img} class="rounded-t "/>
    <div class="flex justify-center p-[20px]">
        <h1 class="bulma-subtitle">{name}</h1>
    </div>
</div>