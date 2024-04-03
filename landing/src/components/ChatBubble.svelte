<script>
    export let placeholder;
    export let time;
    export let name;
    export let message;
    export let start;
</script>

{#if start}
<div class="chat chat-start">
    <div class="avatar placeholder">
        <div class="bg-neutral text-neutral-content rounded-full w-10">
          <span class="text-md">{ placeholder }</span>
        </div>
    </div>
    <div class="chat-header">
      { name }
      <time class="text-xs opacity-50">{ time }</time>
    </div>
    <div class="chat-bubble">{ message }</div>
</div>
{:else}
<div class="chat chat-end">
    <div class="avatar placeholder">
        <div class="bg-neutral text-neutral-content rounded-full w-10">
          <span class="text-md">{ placeholder }</span>
        </div>
    </div>
    <div class="chat-header">
      { name }
      <time class="text-xs opacity-50">{ time }</time>
    </div>
    <div class="chat-bubble chat-bubble-primary">{ message }</div>
</div>
{/if}