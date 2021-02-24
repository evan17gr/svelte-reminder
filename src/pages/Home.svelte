<script>
    import {onMount} from "svelte";
    import {lists} from "../store";
    
    onMount(async () =>{
        const response = await fetch("http://localhost/svelte-api/public/products/initialData");
        const data = await response.json();
        console.log(data);
        $lists = {
            ...$lists,
            ...data
        };
    })
    </script>
    
    
    
    <main>
       
    </main>
    
    <style>
    
    </style>