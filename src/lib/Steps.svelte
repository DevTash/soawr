<script>
    export let direction = 'horizontal'
</script>

<section
    class="steps"
    class:verticle={direction === 'verticle'}
    class:horizontal={direction === 'horizontal'}
>
    <slot></slot>
</section>


<style>
    .steps{
        justify-items: center;
    }

    .horizontal {
        display: grid;
        grid-auto-flow: column;
        column-gap: 0;
        grid-template-columns: repeat(auto-fit, 1fr);
        grid-template-rows: 1fr;
        align-items: center;
    }

    .verticle {
        display: grid;
        grid-auto-flow: row;
        grid-template-rows: repeat(auto-fit, 1fr);
    }
</style>