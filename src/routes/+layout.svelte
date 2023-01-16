<script>

	import './styles.css';
import { gsap } from "gsap";
    import {onMount} from "svelte";

    onMount(()=>{
        gsap.to("#main", {opacity:1, duration:0.1})
    })

</script>

<div id="main" class="opacity-0">
<slot></slot>
</div>