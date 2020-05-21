<script>
import Key from 'components/piano-key/piano-key.component.svelte';

//create a synth and connect it to the master output (your speakers)
var synth = new Tone.Synth().toMaster()
</script>


<Key synth={synth} note="C3" signature="8n" keybinding="z" />
<Key synth={synth} note="D3" signature="8n" keybinding="x" />
<Key synth={synth} note="E3" signature="8n" keybinding="c" />
<Key synth={synth} note="F3" signature="8n" keybinding="v" />
<Key synth={synth} note="G3" signature="8n" keybinding="b" />
<Key synth={synth} note="A3" signature="8n" keybinding="n" />
<Key synth={synth} note="B3" signature="8n" keybinding="m" />