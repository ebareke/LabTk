<!DOCTYPE html>
<html>

<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>LabTk</title>
  <link rel="stylesheet" href="https://stackedit.io/style.css" />
</head>

<body class="stackedit">
	 <h1 id="welcome-to-labtk"> LabTk </h1>
  <div class="stackedit__left">
    <div class="stackedit__toc">
      

<li><a href="#logging-to-your-regional-cc-cloud">Logging to your regional CC cloud</a></li>
<li><a href="#setting-your-environment">Setting your environment</a></li>
</ul>
</li>
<li></li>
<li><a href="#what-is-covered-here-">What is covered here ?</a>
<ul>
<li><a href="#introductory-hands-ons">Introductory Hands-ons</a></li>
<li><a href="#preparing-analyses">Preparing analyses</a></li>
</ul>
</li>
<li>
<ul>
<li><a href="#exomegenome-analyses">Exome/Genome analyses</a></li>
</ul>
</li>
<li>
<ul>
<li><a href="#transcriptomic-analyses">Transcriptomic analyses</a></li>
</ul>
</li>
<li>
<ul>
<li><a href="#epigenetic-analyses">Epigenetic analyses</a></li>
</ul>
</li>
</ul>

</div>
  </div>
  <div class="stackedit__right">
    <div class="stackedit__html">
      <h1 id="welcome-to-labtk">Welcome to LabTk!</h1>
<p>Hi! This repository is used to introduce students with High Performance Computing (HPC), Next Generation Sequence (NGS) file formats, NGS data analysis (DNASeq, RNASeq, microRNA, ChIPSeq, WGBS…), data visualization, and interpretation…</p>
<p>It is assumed that, if you are reading this, you already received your Compute Canada (CC) account, otherwise, follow these  <a href="https://docs.computecanada.ca/wiki/Compute_Canada_Documentation">Instructions!</a></p>
<h2 id="logging-to-your-regional-cc-cloud">Logging to your regional CC cloud</h2>
<p>All along this repository, we will assume that you will be using <strong>Graham</strong> cluster. Note that you can do the same to any of the CC clusters, be it <strong>Cedar</strong>, <strong>Beluga</strong> …</p>
<pre><code>ssh &lt;your_username&gt;@graham.computecanada.ca
ssh &lt;your_username&gt;@graham.sharcnet.ca
</code></pre>
<h2 id="setting-your-environment">Setting your environment</h2>
<p>Your supervisor was assigned a 7-digit <strong>Project Number</strong> on <strong>Graham</strong>, make sur that you know this number.<br>
You will need it to set your working environment and know your lap (and PI) project space.<br>
If Dr.Tetreault Project Number is <strong>6019267</strong>, the project space will be:</p>
<pre><code>/project/6019267/
</code></pre>
<p>You should see your own folder (where you can store intermediate results) inside the project space appearing as:</p>
<pre><code>/project/6019267/&lt;your_username&gt;
</code></pre>
<p>Note that once you finish your analyses, the final results should be pushed into the lab shared folder, named:</p>
<pre><code>/project/6019267/lab/projects/&lt;new_project_name&gt;
</code></pre>
<h3 id="lets-now-configure-your-environment.">Let’s now configure your environment.</h3>
<p>There are a lot of bioinformatics tools and yo will not need to set up any. You will just need to pre-load the appropriate location in your <strong>~/.bash_profile</strong>. Copy and paste the code below in your ~/.bash_profile and do not try to change any code if you do not understand its meaning. We will cover later in the lab, all the code meanings.</p>
<pre><code>if [ -f ~/.bashrc ]; then
	. ~/.bashrc
fi

export PATH="/project/6019267/singularity/1.1.0/images/bin:$PATH"
</code></pre>
<h1 id="section-1"></h1>
<h1 id="what-is-covered-here-">What is covered here ?</h1>
<h2 id="introductory-hands-ons">Introductory Hands-ons</h2>
<ul>
<li class="task-list-item"><input type="checkbox" class="task-list-item-checkbox" disabled=""> Introduction to Linux and Bash Programming</li>
</ul>
<blockquote>
<p><a href="">A quick look at Unix/Linux commands</a><br>
<a href="">First steps in Bash programming</a></p>
</blockquote>
<h2 id="preparing-analyses">Preparing analyses</h2>
<ul>
<li class="task-list-item"><input type="checkbox" class="task-list-item-checkbox" disabled=""> Pre-processing step (QC, DESIGN and YAML files)</li>
</ul>
<blockquote>
<p><a href="">Pre-alignment QC</a>.<br>
<a href="">Preparing your DESIGN file</a><br>
<a href="">Build your YAML config file</a>.</p>
</blockquote>
<h1 id="section-2"></h1>
<h2 id="exomegenome-analyses">Exome/Genome analyses</h2>
<ul>
<li class="task-list-item"><input type="checkbox" class="task-list-item-checkbox" disabled=""> DNASeq processing (<strong>erm</strong> workflows)</li>
</ul>
<blockquote>
<p><a href=""> SNV calling workflow</a>.<br>
<a href="">Structural variant workflow</a>.<br>
<a href="">HLA-typing workflow</a>.</p>
</blockquote>
<ul>
<li class="task-list-item"><input type="checkbox" class="task-list-item-checkbox" disabled=""> DNASeq post-processing (QC Review, Differential Expression, Alternative Splicing, PolyAdenylation analysis)</li>
</ul>
<blockquote>
<p><a href="">Post-erm QC Review</a>.<br>
<a href="">Functionally annotating variants</a>.<br>
<a href="">Prioritizing variants</a>.</p>
</blockquote>
<h1 id="section-3"></h1>
<h2 id="transcriptomic-analyses">Transcriptomic analyses</h2>
<ul>
<li class="task-list-item"><input type="checkbox" class="task-list-item-checkbox" disabled=""> RNASeq processing (<strong>erm</strong> workflows)</li>
</ul>
<blockquote>
<p><a href=""> mRNA workflow</a>.<br>
<a href="">microRNA workflow</a>.<br>
<a href="">single cell RNA workflow</a>.</p>
</blockquote>
<ul>
<li class="task-list-item"><input type="checkbox" class="task-list-item-checkbox" disabled=""> mRNA post-processing (QC Review, Differential Expression, Alternative Splicing, PolyAdenylation analysis)</li>
</ul>
<blockquote>
<p><a href="">Post-erm QC Review</a>.<br>
<a href="">Differential Expression Analysis</a>.<br>
<a href="">Alternative Splicing Analysis</a>.</p>
</blockquote>
<h1 id="section-4"></h1>
<h2 id="epigenetic-analyses">Epigenetic analyses</h2>
<ul>
<li class="task-list-item"><input type="checkbox" class="task-list-item-checkbox" disabled=""> ChIPSeq/WGBS processing (<strong>epi</strong> workflows)</li>
</ul>
<blockquote>
<p><a href=""> ChIPSeq workflow</a>.<br>
<a href="">WGBS workflow</a>.</p>
</blockquote>
<ul>
<li class="task-list-item"><input type="checkbox" class="task-list-item-checkbox" disabled=""> ChIPSeq/WGBS post-processing (QC Review, Peakness Analysis, Differential and Partial Methylation analyses)</li>
</ul>
<blockquote>
<p>TODO</p>
</blockquote>

    </div>
  </div>
</body>

</html>


