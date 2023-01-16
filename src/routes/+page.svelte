<script>
import {gsap} from "gsap"
import {ScrollTrigger} from "gsap/dist/ScrollTrigger"
import {onMount} from "svelte"
import Second from "$lib/sections/Second.svelte";

onMount(()=>{
gsap.registerPlugin(ScrollTrigger);

let tl = gsap.timeline({
      scrollTrigger: {
        trigger: ".first",
        start: "top top",
        pin: true,
        pinSpacing: true,
        scrub: 1,
        end: "+=100%",
      },
    });
    tl.from("#contents",{opacity:0})
    .to("#contents", { opacity: 0 });

  //   let times = gsap.timeline({
  //     scrollTrigger: {
  //       trigger: ".second",
  //       start: "top top",
  //       pin: true,
  //       pinSpacing: true,
  //       scrub: 1,
  //       end: "+=100%",
  //     },
  //   });
  // times.from("#contents_second",{opacity:0})
  //   times.to("#contents_second", { opacity: 0 })

})
</script>

<div
  class="first h-screen w-full  relative flex flex-row justify-center items-center  bg-blue-800"
>
  <div id="contents" class="flex flex-col w-full items-center mt-10">
    <div
      id="mission"
      class="text-5xl  text-white font-michroma pb-4 text-center"
    >
      Home Page
    </div>
    
  </div>

 
</div>

<Second/>
<!-- 
<div
  class="second h-screen w-full items-center  relative flex flex-row justify-center  bg-blue-800"
>
 <div class="text-5xl text-white" id="contents_second"> Second Section </div>

 
</div> -->