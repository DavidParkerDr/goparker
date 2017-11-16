---
title: My DIY eGPU project – Benchmarking
author: David Parker
date: 2012-07-26T22:44:00+00:00
tags: ["eGPU"]
---
Well, I have done a spot of benchmarking. Specifically using 3DMark06 and the Resident Evil 5 benchmarking tool. If you are wondering what I am talking about here is an <a href="http://www.goparker.com/2012/07/my-diy-egpu-project-introduction.html" target="_blank">introduction</a> and a <a href="http://www.goparker.com/2012/07/my-diy-egpu-project-delivery-and-test.html" target="_blank">follow-up</a>.
  
I guess a brief recap wouldn’t be out of place. I have a laptop with integrated graphics. This severely limits the games that I can play. This makes me sad. I have read that I can put together an adapter that plugs in to the ExpressCard slot in my laptop that allows me to use a desktop GPU to power the graphics. This makes me happy.
  
Now, to the benchmarks. First 3DMark06: <a href="http://3dmark.com/3dm06/16794776" target="_blank">before</a> and <a href="http://3dmark.com/3dm06/16794662" target="_blank">after</a>.

<div id="scid:8747F07C-CDE8-481f-B0DF-C6CFD074BF67:65c3ee47-7ab3-4d90-b7b7-cfe2e4861e1f" class="wlWriterEditableSmartContent" style="display:inline;float:none;margin:0;padding:0;">
  <a title="For the link averse: before (left) and after (right)" href="http://lh3.ggpht.com/-ZPYqCZpxgAU/UBHIdOvJ0zI/AAAAAAAAAKo/Go2LQthUoSo/gpu13-8x6.png?imgmax=800" rel="thumbnail"><img src="http://lh6.ggpht.com/-ZymPyu8FgEg/UBHId0Cdq_I/AAAAAAAAAKs/0byAkG32rlc/gpu13%25255B7%25255D.png?imgmax=800" alt="" width="580" height="291" border="0" /></a>
</div>

Not bad I think. A threefold increase from 1207 to 3654 on the 3DMark06 hand-wavy score of magic beans. Next, bring on to the Zombies!
  
The Resident Evil 5 benchmark program runs through a fixed and variable scene and logs the average frames-per-second (fps). The first of the results is the fixed scene where the integrated GPU managed a shameful 8.0fps, soundly thrashed by the eGPU at 23.8fps (though still on the low side for playability).

<div id="scid:8747F07C-CDE8-481f-B0DF-C6CFD074BF67:eb8c6032-22d7-4981-ab5d-3eb4c24b3827" class="wlWriterEditableSmartContent" style="display:inline;float:none;margin:0;padding:0;">
  <a title="For the fixed scene: before (top) and after (bottom)" href="http://lh6.ggpht.com/-_xQ0p0jv-eY/UBHIjO5gaiI/AAAAAAAAAK4/g7dzz74SHCM/gpu16-8x6.png?imgmax=800" rel="thumbnail"><img src="http://lh4.ggpht.com/-WQGi1Yi05_c/UBHIlpMgHII/AAAAAAAAALA/CMc-JiR0W0o/gpu16%25255B5%25255D.png?imgmax=800" alt="" width="580" height="538" border="0" /></a>
</div>

For the variable scene another pleasing result. Up from an unplayable 9.6fps to 40.8fps which is pretty respectable.

<div id="scid:8747F07C-CDE8-481f-B0DF-C6CFD074BF67:5c4fb99c-b408-46f1-b5cb-8cdf271f24c3" class="wlWriterEditableSmartContent" style="display:inline;float:none;margin:0;padding:0;">
  <a title="For the variable scene: before (top) and after (bottom)" href="http://lh5.ggpht.com/-_EiejkF93EE/UBHIqD77HqI/AAAAAAAAALI/SaH6k15098s/gpu15-8x6.png?imgmax=800" rel="thumbnail"><img src="http://lh4.ggpht.com/-BqGdhfIrJAU/UBHItrDAY4I/AAAAAAAAALQ/3Knz37GQk7U/gpu15%25255B9%25255D.png?imgmax=800" alt="" width="580" height="561" border="0" /></a>
</div>

And now for the test that makes it all worth while, the one we (I) have been waiting for. Can I play DayZ on my laptop? YES! I am very pleased. Next things on the to do list for this project are: buy a graphics card (almost certainly second hand from eBay) to replace the borrowed one I was testing with, and construct some kind of enclosure to clear my desk of the precariously balanced computer componentry from this project. For the graphics card I am aiming for something like the Nvidia GTX460 which I understand has a good performance-to-value ratio. When I do I will rerun the benchmarks (they should have improved) and let you know how it goes. Same goes for the enclosure construction and modding.