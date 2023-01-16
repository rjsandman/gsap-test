<script>
import {gsap} from "gsap"
import {ScrollTrigger} from "gsap/dist/ScrollTrigger"
import {onMount} from "svelte"

onMount(()=>{
gsap.registerPlugin(ScrollTrigger);

let times = gsap.timeline({
      scrollTrigger: {
        trigger: ".second",
        start: "top top",
        pin: true,
        pinSpacing: true,
        scrub: 1,
        end: "+=100%",
      },
    });
  times.from("#contents_second",{opacity:0})
    times.to("#contents_second", { opacity: 0 })

})
</script>

<div
  class="second h-screen w-full items-center  relative flex flex-row justify-center  bg-blue-800"
>
 <div class="text-5xl text-white" id="contents_second"> Second Section </div>

 
</div>