---
title: My DIY eGPU Project – Speed boost
author: David Parker
date: 2012-08-01T09:55:00+00:00
tags: ["eGPU"]
---
This morning, some lovely person using the handle Burger commented on one of my <a href="http://www.goparker.com/2012/07/my-diy-egpu-project-benchmarking.html?showComment=1343809982848#c9044794735657189722" target="_blank">earlier posts</a> suggesting that if I connect the eGPU setup after boot-up is complete then I should get a significant boost due to PCIe compression. I little bit of Googling reveals a bit more detail <a href="http://forum.notebookreview.com/e-gpu-external-graphics-discussion/418851-diy-egpu-experiences-123.html#post6542661" target="_blank">here</a>, but it seems that you need to have a ‘modern’ Intel integrated GPU in combination with one of a fairly narrow range of Nvidia kit.

Luckily that is what I have so I thought I would give it a try (<a href="http://3dmark.com/3dm06/16803943" target="_blank">online 3DMark06 results here</a>).

<div id="scid:8747F07C-CDE8-481f-B0DF-C6CFD074BF67:0d3b479d-7487-4c41-a541-0a2651504618" class="wlWriterEditableSmartContent" style="margin:0;display:inline;float:none;padding:0;">
  <a title="Just wow" href="http://lh3.ggpht.com/-tfgqVh96-TI/UBj9KAqunwI/AAAAAAAAAMY/14remLKD6sc/gpu23-8x6.png?imgmax=800" rel="thumbnail"><img src="http://lh4.ggpht.com/-B3-mWwjWw7w/UBj9LaKyPlI/AAAAAAAAAMg/CKj4woEZ7vc/gpu23%25255B3%25255D.png?imgmax=800" alt="" width="580" height="477" border="0" /></a>
</div>

That is a pretty staggering leap to 12804 3DMarks (from 7021 3DMarks) and it hits the magic number of being more than 10 times higher than the score from using the integrated GPU on its own (1207 3DMarks). So thanks Burger!

For some reason it didn’t really make any difference to the Resident Evil 5 tests (which is why I have not included the results screenshot here).