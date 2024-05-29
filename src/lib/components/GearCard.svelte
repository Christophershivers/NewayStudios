<script lang="ts">
    export let img;
    export let name;
</script>

<div class="  rounded shadow-md h-[200px] w-[200px] relative border border-gray-300 dark:border-gray-700">
    <img src={img} alt="canon"/>
    <div class="opacity-0 hover:opacity-100 duration-300 absolute inset-0 z-10 flex justify-center items-center text-md text-white font-semibold h-[200px] w-[200px] bg-black/70 group-hover:bg-black/90">{name}</div>
</div>