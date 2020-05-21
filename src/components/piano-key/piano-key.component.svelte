<script>

export let synth;
export let note;
export let signature;
export let keybinding;

let isPressed;

const handleKeyClick = () => {
    synth.triggerAttackRelease(note, signature);
    isPressed = true;
};
const handleKeydown = event => {
    const key = event.key;
    if (key === keybinding) {
        handleKeyClick();
    } else {
        isPressed = false;
    }
};
</script>

<style>
    .pressed {
        background-color: #333333;
        color: #ffffff;
    }
</style>

<svelte:window on:keydown={handleKeydown} />
<button class={isPressed ? 'pressed' : ''} on:click={handleKeyClick}>{note}</button>