<script>
  import { getContext } from "svelte";

  export let text;
  export let color;
  export let textColor;
  export let icon;
  export let hideable;
  export let size = "medium";

  const { styleable } = getContext("sdk");
  const component = getContext("component");

  let hidden;
  let sizeClass;

  $: sizeClass = `size-${size}`;

  $: $component.styles = {
    ...$component.styles,
    normal: {
      ...$component.styles.normal,
      "--super-tag-color": color,
      "--super-tag-text-color": textColor,
      "--super-tag-width": icon ? "6rem" : "5rem",
    },
  };
</script>

<!-- svelte-ignore a11y-click-events-have-key-events -->
<!-- svelte-ignore a11y-no-static-element-interactions -->
{#if !hidden}
  <div class="super-tag {sizeClass}" use:styleable={$component.styles}>
    {#if icon}
      <i class={icon} />
    {/if}
    <span class="tag-text">{text ?? ""}</span>
    {#if hideable}
      <i class={"ri-close-line close"} on:click={() => (hidden = true)} />
    {/if}
  </div>
{/if}

<style>
  .super-tag {
    flex: none;
    background-color: var(--super-tag-color);
    color: var(--spectrum-global-color-gray-900);
    width: fit-content;
    border-radius: 0.25rem;
    display: flex;
    align-items: center;
    justify-content: center;
    gap: 0.5rem;
    min-width: 3rem;
  }
  
  .size-small {
    height: 1.25rem;
    padding: 0rem 0.5rem;
    font-size: 10px;
  }
  
  .size-medium {
    height: 1.65rem;
    padding: 0rem 0.75rem;
    font-size: 12px;
  }
  
  .size-large {
    height: 2rem;
    padding: 0rem 1rem;
    font-size: 14px;
  }

  .tag-text {
    font-weight: 600;
    color: var(--super-tag-text-color, var(--spectrum-global-color-gray-900));
    text-overflow: ellipsis;
    overflow: hidden;
    white-space: nowrap;
  }
  
  .size-small .tag-text {
    font-size: 11px;
  }
  
  .size-medium .tag-text {
    font-size: 13px;
  }
  
  .size-large .tag-text {
    font-size: 15px;
  }

  .close {
    color: var(--spectrum-global-color-gray-800);

    &:hover {
      cursor: pointer;
      color: var(--spectrum-global-color-gray-900);
    }
  }
  
  .size-small .close {
    font-size: 9px;
  }
  
  .size-medium .close {
    font-size: 11px;
  }
  
  .size-large .close {
    font-size: 13px;
  }
</style>
