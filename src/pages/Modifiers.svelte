<script>
    import { each } from "svelte/internal";
    import {onMount} from "svelte";
    import {lists} from "../store";
</script>
    
<main>
    {#each $lists.departments as item}
        <div class="card" style="width: 18rem;">
            <div class="card-body">
                <h5 class="card-title">{item.name}</h5>
                <h6 class="card-subtitle mb-2 text-muted">Card subtitle</h6>
                <p class="card-text">{item.department_id}</p>
                <a href="#" class="card-link">Card link</a>
                <a href="#" class="card-link">Another link</a>
            </div>
        </div>
    {/each}
</main>

<style>
    main{
        display: flex;
        margin:5% 3%;
        justify-content: center;
    }
    
    .card{
        margin:0 1%;
    }
</style>