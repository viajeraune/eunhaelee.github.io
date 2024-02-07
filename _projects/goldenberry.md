<!-- ---
layout: page
title: Inclusive innovation case study
description: Rehabilitating Goldenberry Production in the Ecuadorian Andes With Regenerative Agriculture
image: assets/images/net.jpeg
nav-menu: false
show_tile: false
order: 6
--- -->

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
<p>This case study describes an inclusive local innovation process involving smallholder farming communities in the Ecuadorian Andes engaged in producing organic goldenberries for export. In early 2020, as the global COVID-19 pandemic started to disrupt supply chains, health, and livelihoods around the world, these communities found themselves facing a novel and highly aggressive plant disease referred to colloquially as "mancha morada." The case study describes a co-innovation process led by an Ecuadorian nonprofit organization, Aliados, through which these communities, working in collaboration with Aliados technicians and other local stakeholders, developed a successful approach to preventing and controlling mancha morada using principles and practices from regenerative agriculture. Drawing on original primary research, the case study describes the innovation process in depth, following the chronology of the case as described by research participants to identify key turning points, factors contributing to the success of this process, and the results these farming communities have been able to jointly achieve.</p>


<p><a href="https://www.researchgate.net/publication/362605228_Rehabilitating_Goldenberry_Production_in_the_Ecuadorian_Andes_With_Regenerative_Agriculture" class="button">See paper on ResearchGate</a></p>


<h2 id="content">Highlights</h2>
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

<!-- <p><a href="">See paper on arxiv</a></p> -->

<h4>Details</h4>
<p>This research was completed as a final project for the graduate course 6.S898 Deep Learning at MIT. I am the sole author of the project and paper. </p>


</div>
</section>


</div>
