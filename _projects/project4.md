---
layout: page
title: Continual Learning Research Project
description: How model size impacts catastrophic forgetting
image: assets/images/pic04.jpg
nav-menu: false
show_tile: true
order: 4
---

<!-- Main -->
<div id="main" class="alt">

<!-- One -->
<section id="one">
	<div class="inner">
		<header class="major">
			<h1>How does model size impact catastrophic forgetting in online continual learning? [Research paper]</h1>
		</header>

<!-- Content -->
<h2 id="content">About</h2>

<p>This study investigates the impact of model size on online continual learning performance, with a focus on catastrophic forgetting. Employing ResNet architectures of varying sizes and a slim version of ResNet18, the research examines how network depth and width affect model performance in class-incremental learning using the SplitCIFAR-10 dataset. Key findings reveal that larger models do not guarantee better continual learning performance; in fact, they often struggle more in adapting to new tasks, particularly in online settings. Surprisingly, the slim ResNet18 frequently outperformed its larger counterparts. These results challenge the notion that larger models inherently mitigate catastrophic forgetting, highlighting the nuanced relationship between model size and continual learning efficacy. This study contributes to a deeper understanding of model scalability and its practical implications in continual learning scenarios.</p>
<p>This research project was done as a final project for a graduate course on Deep Learning (6.S898 Deep Learning) at MIT. The objective was to complete an original research project exploring a scientific research question that leads to new insights and understanding, related to but going beyond the topics learned in the course. I was the sole author of the project and paper. </p>

<h2 id="content">Highlights</h2>
<div class="row">
	<div class="6u 12u$(small)">
		<img src="{{ '/assets/images/AAA_on_off.png' | relative_url }}" alt="chart" data-position="center center" />
	</div>
	<div class="6u$ 12u$(small)">
		<h3>Average Anytime Accuracy (AAA) decreases as model size increases</h3>
		<p>This chart shows Average Anytime Accuracy (AAA) of different sized ResNets in online and offline continual learning. Average Anytime Accuracy (AAA) decreases with model size, with a sharper drop from ResNet34 to ResNet50. The decrease in AAA is more significant in online learning than offline learning.</p>
	</div>
</div>

<div class="row">
	<div class="6u 12u$(small)">
		<img src="{{ '/assets/images/stream_acc1.png' | relative_url }}" alt="chart" data-position="center center" />
	</div>
	<div class="6u$ 12u$(small)">
		<h3>Accuracy of larger models grow at a slower pace when training</h3>
		<p>When looking at average accuracy for validation stream for online CL setting (Chart 2), we see that the rate to which accuracy increases with each task degrade with larger models. Slim-ResNet18 shows the highest accuracy and growth trend. This could indicate that larger models are worse at generalizing to a class-incremental learning scenario.</p>
	</div>
</div>

<div class="row">
	<div class="6u 12u$(small)">
		<img src="{{ '/assets/images/forgetting_curves.png' | relative_url }}" alt="chart" data-position="center center" />
	</div>
	<div class="6u$ 12u$(small)">
		<h3>Forgetting increases as model size increases</h3>
		<p>This differences in forgetting between online and offline CL setting is aligned with the accuracy metrics earlier, where the performance of ResNet50 decreases more starkly in the online CL setting.</p>
	</div>
</div>

<div class="row">
	<div class="6u 12u$(small)">
		<img src="{{ '/assets/images/saliency_online.png' | relative_url }}" alt="chart" data-position="center center" />
	</div>
	<div class="6u$ 12u$(small)">
		<h3>Saliency maps reveal hints on how the model reads the inputs</h3>
		<p>When it comes to the ability to highlight intuitive areas of interest in the images, there seemed to be a noticeable improvement from ResNet18 to ResNet34, but this was not necessarily the case from ResNet34 to ResNet50.</p>
	</div>
</div>
	<!-- Break -->
	<!-- <div class="4u 12u$(medium)">
		<h3>Interdum sapien gravida</h3>
		<p>Nunc lacinia ante nunc ac lobortis. Interdum adipiscing gravida odio porttitor sem non mi integer non faucibus ornare mi ut ante amet placerat aliquet. Volutpat eu sed ante lacinia sapien lorem accumsan varius montes viverra nibh in adipiscing blandit tempus accumsan.</p>
	</div>
	<div class="4u 12u$(medium)">
		<h3>Faucibus consequat lorem</h3>
		<p>Nunc lacinia ante nunc ac lobortis. Interdum adipiscing gravida odio porttitor sem non mi integer non faucibus ornare mi ut ante amet placerat aliquet. Volutpat eu sed ante lacinia sapien lorem accumsan varius montes viverra nibh in adipiscing blandit tempus accumsan.</p>
	</div>
	<div class="4u$ 12u$(medium)">
		<h3>Accumsan montes viverra</h3>
		<p>Nunc lacinia ante nunc ac lobortis. Interdum adipiscing gravida odio porttitor sem non mi integer non faucibus ornare mi ut ante amet placerat aliquet. Volutpat eu sed ante lacinia sapien lorem accumsan varius montes viverra nibh in adipiscing blandit tempus accumsan.</p>
	</div> -->

<hr class="major" />



</div>
</section>


</div>
