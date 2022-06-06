<script>
    export let href = ''
    export let alt = ''
</script>

{#if !!href}
    <a {href} {alt}>
        <slot></slot>
    </a>
{:else}
    <button>
        <slot></slot>
    </button>
{/if}

<style>
    button {
        appearance: none;
        border: none;
    }

    button,
    a 
    {
        background: #e34612;
        padding: 1rem;
        border-radius: 10px;
        color: var(--pure-white);
        display: grid;
        justify-content: center;
        align-content: center;
        font-size: 1.25rem;
        font-weight: 900;
        text-transform: capitalize;
    }
</style>