<script>
	import Hoverable from "./hoverable.svelte";
</script>



<h3>Expierence</h3>

<div class="expierence">
    <div class="expierence_date">1.06.2022-present</div>
    <div class="expierence_name">MagnIT</div>
    <div class="expirience_details">
        <Hoverable let:hovering={active}>
            <div class:active>
                {#if active}
                    <p>Work as Python backend-developer. Organised switching to the Minio Cloud System.</p>
                    <p>Worked on the creation of handbooks and models.</p>
                {:else}
                    <p>Work as Python backend-developer...</p>
                {/if}
            </div>
        </Hoverable>
    </div> 
</div>

<style>
	.active {
		background-color: #00a2ff4d;
		color: white;
        padding: 0 1em 0 1em  ;
	}
</style>