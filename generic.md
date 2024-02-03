---
layout: post
title: generic
description: Lorem ipsum dolor est
image: assets/images/net.jpeg
nav-menu: false
show_tile: false
---



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

<hr class="major" />





Donec eget ex magna. Interdum et malesuada fames ac ante ipsum primis in faucibus. Pellentesque venenatis dolor imperdiet dolor mattis sagittis. Praesent rutrum sem diam, vitae egestas enim auctor sit amet. Pellentesque leo mauris, consectetur id ipsum sit amet, fergiat. Pellentesque in mi eu massa lacinia malesuada et a elit. Donec urna ex, lacinia in purus ac, pretium pulvinar mauris. Curabitur sapien risus, commodo eget turpis at, elementum convallis elit. Pellentesque enim turpis, hendrerit.

Lorem ipsum dolor sit amet, consectetur adipiscing elit. Duis dapibus rutrum facilisis. Class aptent taciti sociosqu ad litora torquent per conubia nostra, per inceptos himenaeos. Etiam tristique libero eu nibh porttitor fermentum. Nullam venenatis erat id vehicula viverra. Nunc ultrices eros ut ultricies condimentum. Mauris risus lacus, blandit sit amet venenatis non, bibendum vitae dolor. Nunc lorem mauris, fringilla in aliquam at, euismod in lectus. Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas. In non lorem sit amet elit placerat maximus. Pellentesque aliquam maximus risus, vel sed vehicula.

Interdum et malesuada fames ac ante ipsum primis in faucibus. Pellentesque venenatis dolor imperdiet dolor mattis sagittis. Praesent rutrum sem diam, vitae egestas enim auctor sit amet. Pellentesque leo mauris, consectetur id ipsum sit amet, fersapien risus, commodo eget turpis at, elementum convallis elit. Pellentesque enim turpis, hendrerit tristique lorem ipsum dolor.
