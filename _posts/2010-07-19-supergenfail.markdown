---
title: How to get started in computational biology
tags:  []
layout: post
---

_Audience: Anyone interested in comp bio without any experience_

### Where do I begin?

Science should always begin with a question. Here are some examples:
- Why do naked mole rats live 10x longer than other rodents?
- What are early biomarkers of Alzheimers Disease?
- How does the immune system develop?
- What drug can inhibit this protein?

Then you need to figure out what data you need to answer your question. While it may be useful to learn the basics of programming before beginning, I think its best to have a project in mind. When others just try to learn comp bio, they will often forget or learn skills that won't be used on their future project. 

### What types of tools do I use?

That is highly dependent on the question you ask. There are thousands of tools. One of the best ways is to find a paper on pubmed that asked a similar question.

### What language do I need to know?

The software packages for upstream analysis are often run at the command line using Bash. The downstream analysis packages are usually run in python or R.

### What is a pipeline?

A bioinformatics pipeline is a series of software algorithms that converts your raw data into your results. In RNA sequencing, we will convert our raw reads from the Illumina sequencer into transcript levels. I included a simple outline with some example code. 

raw data: ATGGCCTCTGATAGTC

> find out where it matches in the genome

{% highlight bash %}
bowtie2 -x genome -1 /PATH/to/reads/reads_1.fq -2 /PATH/to/reads/reads_2.fq -S output.sam
{% endhighlight %}

> count the number of reads in each gene

{% highlight bash %}
featureCounts -T 5 -t exon -g gene_id -a annotation.gtf -o counts.txt output.sam
{% endhighlight %}

This yeilds a count matrix that we can use to answer many questions.

### What are some resources?

Learn coding basics: Codecademy
Find seq data: NCBI GEO
Troubleshoot: Biostars






