<script>
  let selectedState = '';
</script>

<div class="calculator">
<div class="machine">
<h3> How many people rely on SNAP benefits in this state? </h3>
  <label for="state">Choose a state</label>
  <input list="state-options" id="state" name="state" bind:value={selectedState} />
  <datalist id="state-options">
    <option value="Arizona">Arizona</option>
    <option value="Alaska">Alaska</option>
    <option value="Alabama">Alabama</option>
  </datalist>
</div>
<div class="answer">
  {#if selectedState === "Arizona"}
    <p>  In Arizona. <strong> 659,121 </strong> people, about 9% of the state population, rely on SNAP benefits.  </p>
  {/if}
 {#if selectedState === "Alaska"}
    <p>  In Alaska, <strong> 65,660 </strong> people, almost 9% of the state population, rely on SNAP benefits. </p>
  {/if}
  {#if selectedState === "Alabama"}
  <p> In Alabama <strong> 707,340 </strong> people, about 14% of the state population,rely on SNAP benefits. </p>
  {/if}
</div>
</div>

<style>
  .calculator {
    background-color: var(--color-light-gray);
    display: block;
    gap: 0.75rem;
    margin: 2rem 0;
    padding: 1rem;
    
  }
  select {
    margin-top: 3rem;
    margin-bottom: 3rem;
    padding: 3rem;
  }
.answer {
    margin-top: 1rem;
    margin-bottom: 1rem;
    padding: 3rem;

}

</style>