<script lang="typescript">
  export let id: String;
  export let name: String;
  export let weight: Number;

  let tookBreak: Boolean = false;
</script>

<form class="exercise">
  <h3>{name}</h3>
  <div>
    <label for={`reps-${id}`}>Reps</label>
    <input type="number" id={`reps-${id}`} />
  </div>

  {#if weight}
    <label for={`weight-${id}`}>Weight</label>
    <input type="number" id={`weight-${id}`} />
  {/if}

  <div>
    <label for={`break-${id}`}>Break?</label>
    <input type="checkbox" id={`break-${id}`} bind:checked={tookBreak} />
  </div>

  {#if tookBreak}
    <div class="reps-after-break">
      <label for={`reps-after-break-${id}`}>Reps after break</label>
      <input type="number" id={`reps-after-break-${id}`} />
    </div>
  {/if}

  <div>
    <label for={`notes-${id}`}>Notes</label>
    <input type="text" id={`notes-${id}`} />
  </div>

  {#if weight}
    <div>
      <label for={`do-more-${id}`}>More weight next time?</label>
      <input type="checkbox" id={`do-more-${id}`} />
    </div>
  {/if}

  <button type="submit">Done</button>
</form>
