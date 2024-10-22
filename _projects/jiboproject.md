---
layout: page
title: Constructing a Schema for Social Robots Using Knowledge Graphs
description: Can we give social robots memory and personality using graph RAG?
image: assets/images/jiboproject/robotsketch.png
nav-menu: false
show_tile: true
order: 11
---

<!-- Main -->
<div id="main" class="alt">

<!-- One -->
<section id="one">
	<div class="inner">
		<header class="major">
			<h1>Constructing a Schema for Social Robots Using Knowledge Graphs</h1>
		</header>
		<!-- {% if page.image %}
        <span class="image main">
        <img src="{{ site.baseurl }}/{{ page.image }}" alt="sketched version of a social robot" />
        <figcaption>Colorful nets against a black background</figcaption>
        </span>{% endif %} -->
        


<!-- Content -->
<h2 id="content">Overview</h2>
<p>In this research project, we explore how mental models and schemas can be effectively applied to social robots using the construction of knowledge graphs based on past interactions, ensuring that their future interactions are not only natural but also reflective of their designed identities. Through this approach, robots can better understand the nuances of human communication and interact in a way that is both informed
and intuitive.</p>


<!-- <p><a href="{{ site.baseurl }}/assets/images/jiboproject/social_robot_schema_paper.pdf" class="button">See paper</a></p> -->

<br />

<h2 id="content">Main contributions</h2>
<p><strong>LLM-Powered Knowledge Graph Creation:</strong> Inspired by how humans acquire, store, and update information through schemas and mental models, we
apply these concepts to Jibo through constructing and updating a knowledge graph (KG) that becomes the knowledge base for Jibo. Moreover, we wanted to mimic Jibo’s personality based on the style deduced from its past interactions. The KG acts a smart RAG model and is in charge of grounding a fine-tuned GPT model on Jibo-specific knowledge.
</p>
<p><strong>LLM-Powered Evaluation Pipeline:</strong> We create a golden dataset of questions and ground truth answers based on the original Jibo single-turn conversation dataset. We use the following metrics adapted from Continuous Eval by Relari.ai:</p>
<ul>
    <li>Correctness: Assesses the overall quality of the output given the question and the ground truth answer.</li>
    <li>Faithfulness: Measures how grounded the answer is based on the retrieved context.</li>
    <li>Relevance Measures: how relevant the output is to the question.</li>
    <li>Style consistency Assesses: the style consistency of the output against the ground truth answer, including tone, verbosity, formality, complexity, and use of terminology.</li>
</ul>

<h2 id="content">Methodology</h2>

<p><strong>1. Construction of the Knowledge Graph:</strong></p>
<ul>
    <li>We employ LLMs to extract entities and relations from the dataset and construct a knowledge graph (KG).</li>
    <li>We augment the KG using LLMs to interpolate among nodes and generate plausible memories for Jibo, guided by prompts engineered to ensure alignment with Jibo's capabilities and limitations and filtering out implausible memories.</li>
</ul>
<p><strong>2. Finetuning:</strong> gpt-3.5-turbo-0125 model on the entire Jibo question answer dataset to mimic Jibo's speech and behavior.</p>
<p><strong>3. Construction of Second-Order Nodes for efficient retrieval</strong></p>
<img src="{{ site.baseurl }}/assets/images/jiboproject/second-order nodes.png" alt="second order nodes of the knowledge graph-based schema" />

<p>The Dataset is made of utterances describing the robot Jibo. The resulting Knowledge Graph is centered around the Jibo node. </p>
<ul>
    <li>When prompting the LLM the context window is easily filled as every query contains the entire graph---all the relations pass through the central node Jibo.</li>
    <li>To redistribute more equally the relations and enable more efficient retrieval, we subdivide the relations of the central Jibo node in Second-Order Nodes that encompass different high-level attributes of Jibo. (e.g. <em>Jibo-likes-holidays</em>, <em>Jibo-likes-sports</em>, <em>Jibo-possessions</em> ... etc)</li>
</ul>

The resulting knowledge graph-based RAG (KG-RAG) pipeline is shown in the following figure:

<img src="{{ site.baseurl }}/assets/images/jiboproject/kg_rag_pipeline.jpeg" alt="knowledge graph RAG pipeline" />


<h2 id="content">Evaluation</h2>
<p>A first qualitative analysis over the results seems to suggest that the answers of the Knowledge Graph respect Jibo persona and prior knowledge. We plan to further evaluate our approach using our evaluation pipeline.</p>

<img src="{{ site.baseurl }}/assets/images/jiboproject/qualitative_results.png" alt="knowledge graph RAG pipeline" />


<hr class="major" />

<iframe src="{{ site.baseurl }}/assets/images/jiboproject/social_robot_schema_paper.pdf" width="100%" height="600px">
        This browser does not support PDFs. Please download the PDF to view it: 
        <a href="{{ site.baseurl }}/assets/images/jiboproject/social_robot_schema_paper.pdf">Download PDF</a>.
        </iframe>

<hr class="major" />

<h4>Details</h4>
<ul>
    <li>Collaborators: Serena Bono, Brian Bailey</li>
	<li>This study was completed as a final project for the graduate course 6.S986 LLMs and beyond at MIT in Spring 2024.</li>
</ul>

</div>
</section>


</div>
