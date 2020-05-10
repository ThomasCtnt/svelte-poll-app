<script>
    export let type = 'primary';
    export let flatened = false;
    export let inversed = false;
</script>

<button class={type} class:flatened={flatened} class:inversed={inversed}>
    <slot></slot>
</button>

<style>
    button {
        border: 0;
        cursor: pointer;
        border-radius: 4px;
        padding: 8px 12px;
        font-weight: bold;
        box-shadow: 1px 2px 3px rgba(0, 0, 0, 0.2);
    }

    .primary {
        background-color: #d91b42;
        color: #fff;
    }

    .secondary {
        background-color: #45C496;
        color: #fff;
    }

    .primary.inversed {
        background-color: #fff;
        color: #d91b42;
        border: 2px solid #d91b42;
    }

    .secondary.inversed {
        background-color: #fff;
        color: #45C496;
        border: 2px solid #45C496;
    }

    .flatened {
        box-shadow: none;
    }
</style>