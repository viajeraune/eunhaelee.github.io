---
layout: page
title: Continual Learning Research Project
description: Deep learning model size and catastrophic forgetting
image: assets/images/net.jpeg
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
			<h1>[Research paper] How does model size impact catastrophic forgetting in online continual learning? </h1>
		</header>
		{% if page.image %}<span class="image main"><img src="{{ site.baseurl }}/{{ page.image }}" alt="colorful nets against black background" /></span>{% endif %}
<!-- Content -->
<h2 id="content">Overview</h2>
<p>Continual learning (CL) aims to enable models to continuously learn from new, non-iid data streams while retaining previously acquired knowledge, facing the stability-plasticity dilemma. Unlike traditional CL models that learn from tasks with stable data distributions in an offline manner, Online Continual Learning (OCL) addresses more realistic scenarios where data arrives in small batches and cannot be revisited after training. OCL requires models to adapt in real-time, balancing between learning new information and preserving old knowledge without the need for access to all past data, often due to privacy or resource constraints.</p>
<p>This study investigates the impact of model size on online continual learning performance, with a focus on catastrophic forgetting. Employing ResNet architectures of varying sizes and a slim version of ResNet18, the research examines how network depth and width affect model performance in class-incremental learning using the SplitCIFAR-10 dataset. Key findings reveal that larger models do not guarantee better continual learning performance; in fact, they often struggle more in adapting to new tasks, particularly in online settings. Surprisingly, the slim ResNet18 frequently outperformed its larger counterparts. These results challenge the notion that larger models inherently mitigate catastrophic forgetting, highlighting the nuanced relationship between model size and continual learning efficacy. This study contributes to a deeper understanding of model scalability and its practical implications in continual learning scenarios.</p>

<h2 id="content">Key findings</h2>
<div class="row">
	<div class="6u 12u$(small)">
		<strong>Accuracy decreases as model size increases</strong>
		<p>Average Anytime Accuracy (AAA) measures the effectiveness of the model across all stages of training, rather than at a single endpoint, offering a more comprehensive view of its learning trajectory.</p>
	</div>
	<div class="6u$ 12u$(small)">
		<img src="{{ '/assets/images/AAA_on_off.png' | relative_url }}" alt="chart" data-position="center center" />
	</div>
</div>

<div class="row">
	<div class="6u 12u$(small)">
		<strong>Accuracy of larger models grow at a slower pace when training</strong>
		<p>The rate to which validation stream accuracy increases with each task degrade with larger models. Slim-ResNet18 shows the highest accuracy and growth trend. This could indicate that larger models are worse at generalizing to a class-incremental learning scenario.</p>
	</div>
	<div class="6u$ 12u$(small)">
		<img src="{{ '/assets/images/stream_acc1.png' | relative_url }}" alt="chart" data-position="center center" />
	</div>
</div>

<div class="row">
	<strong>Forgetting levels show more nuanced results</strong>
		<p>This differences in forgetting between online and offline CL setting is aligned with the accuracy metrics earlier, where the performance of ResNet50 decreases more starkly in the online CL setting. Future studies could increase training cycles to lead to more insights.</p>
	<div class="6u 12u$(small)">
		<img src="{{ '/assets/images/forgetting_online.png' | relative_url }}" alt="chart" data-position="center center" />
	</div>
	<div class="6u$ 12u$(small)">
		<img src="{{ '/assets/images/forgetting_offline.png' | relative_url }}" alt="chart" data-position="center center" />
	</div>
</div>


<strong>Saliency maps reveal hints on how the models read the inputs</strong>
<p>When it comes to the ability to highlight intuitive areas of interest in the images, there seemed to be a noticeable improvement from ResNet18 to ResNet34, but this was not necessarily the case from ResNet34 to ResNet50.</p>
<img src="{{ '/assets/images/saliency_online.png' | relative_url }}" alt="chart" data-position="center center" />

<hr class="major" />

<p><a href="">See paper on arxiv</a></p>

<p>This research project was done as a final project for a graduate course on Deep Learning (6.S898 Deep Learning) at MIT. I am the sole author of the project and paper. </p>



</div>
</section>


</div>
