<script>import "../app.css"; import { Button } from "$lib/components/ui/button";</script>

<style>
    @import "https://cdn.jsdelivr.net/npm/bulma@1.0.0/css/versions/bulma-prefixed.min.css";
</style>


<div class="h-[90px] shadow-md w-[100%] bg-white/30 backdrop-blur-md fixed md:fixed z-10">
    <div class="flex justify-between items-center h-[100%] pl-4 pr-4">
        <div>
            <img src="/IMG-1715.PNG" alt="logo" width="100px"/>
        </div>
        <div>
            <Button class="bg-[#D23A24]"><a href="#" class="text-white">Login</a></Button>
        </div>
    </div>
</div>

<slot></slot>