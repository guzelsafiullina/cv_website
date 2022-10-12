<script>
    import Hoverable from "./hoverable.svelte";
</script>
<h3>Education</h3>
<div class="education">
    <div class="education_year">1.09.2017-31.08.2021</div>
    <div class="education_details">
        <div class="education_name">Moscow Institute of Physics and Technology</div>
        <div class="education_achievments">
            <Hoverable let:hovering={active}>
                <div class:active>
                    {#if active}
                        <ul>
                            <li>Average mark 4.7</li>
                            <li>Courses in Linear Algebra, Advanced mathematics, Physics</li>
                            <li>Participant of ICPS conference</li>
                        </ul>
                    {:else}
                        <p>Got a bachelor degree ...</p>
                    {/if}
                </div>
            </Hoverable>
        </div>

    </div>

</div>
<div class="education">
    <div class="education_year">1.09.2021-present</div>
    <div class="education_details">                
        <div class="education_name">Innopolis University</div>
        <div class="education_achievments">
            <Hoverable let:hovering={active}>
                <div class:active>
                    {#if active}
                        <ul>
                            <li>Average mark 4.5</li>
                            <li>Courses in Machine Learning, Statistics, Optimization</li>
                            <li>Papers for conference 'Non linearity etc</li>
                        </ul>
                    {:else}
                        <p>Got a master degree ...</p>
                    {/if}
                </div>
            </Hoverable>

        </div>
    </div>

</div>

<style>
	.active {
		background-color: #00a2ff4d;
		color: white;
        padding: 0 1em 0 1em  ;
	}
</style>
