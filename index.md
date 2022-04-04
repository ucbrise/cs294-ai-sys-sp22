---
layout: default
---


# Machine Learning Systems (Spring 2022)

* **When**: *Mondays from 1:00 to 4:00*
* **Where**: Soda 405 (and on zoom with with link posted on Slack).
* **Instructor**: [Joseph E. Gonzalez](https://eecs.berkeley.edu/~jegonzal)
* **Co-Instructor**: [Amir Gholami](https://eecs.berkeley.edu/~amirgh)
* **Office Hours:**: Arrange by email.
* **Announcements**: Slack (please send us an email if you are not added yet) 
* **Sign-up to Present**: Every student should sign-up to present in at least three rows and as different roles each time.  Note that the Backup/Scribe presenter may be asked to fill in for one of the other roles with little notice.
* If you have reading suggestions please send a pull request to this course website on [Github](https://github.com/ucbrise/cs294-ai-sys-sp22) by modifying the [index.md](https://github.com/ucbrise/cs294-ai-sys-sp22/blob/master/index.md) file.


## Course Description

The recent success of AI has been in large part due in part to advances in hardware and software systems. These systems have enabled training increasingly complex models on ever larger datasets. In the process, these systems have also simplified model development, enabling the rapid growth in the machine learning community. These new hardware and software systems include a new generation of GPUs and hardware accelerators (e.g., TPU), open source frameworks such as Theano, TensorFlow, PyTorch, MXNet, Apache Spark, Clipper, Horovod, and Ray, and a myriad of systems deployed internally at companies just to name a few. 
At the same time, we are witnessing a flurry of ML/RL applications to improve hardware and system designs, job scheduling, program synthesis, and circuit layouts.  

In this course, we will describe the latest trends in systems designs to better support the next generation of AI applications, and applications of AI to optimize the architecture and the performance of systems. 
The format of this course will be a mix of lectures, seminar-style discussions, and student presentations. 
Students will be responsible for paper readings, and completing a hands-on project. 
For projects, we will strongly encourage teams that contains both AI and systems students.



## New Course Format

Two previous versions of this course were offered in <a href="https://ucbrise.github.io/cs294-ai-sys-sp19/#today">Spring 2019</a>, and <a href="https://ucbrise.github.io/cs294-ai-sys-fa19/#today">Fall 2019</a>.
The format of this third offering is slightly different.  Each week will cover a different research area in AI-Systems.
The lecture will be organized around a mini program committee meeting for the weeks readings. Students will be required to submit detailed reviews
for a subset of the papers and lead the paper review discussions. For some of the topics, we have also invited prominent researchers for each area and they will present
an overview of the field, followed by discussions raised during the "committee meeting".
The goal of this new format is to both build a mastery of the material and also to
develop a deeper understanding of how to evaluate and review research and hopefully provide insight into how to write better papers. 


## Course Syllabus
{% capture dates %}
1/24/22
1/31/22
2/07/22
2/14/22
2/21/22
2/28/22
03/07/22
03/14/22
03/21/22
03/28/22
04/04/22
04/11/22
04/18/22
04/25/22
05/02/22
05/09/22
{% endcapture %}
{% assign dates = dates | split: " " %}

This is a tentative schedule. Specific readings are subject to change as new material is published.

<a href="#today"> Jump to Today </a>

<table class="table table-striped syllabus">
<thead>
   <tr>
      <th style="width: 5%"> Week </th>
      <th style="width: 10%"> Date </th>
      <th style="width: 85%"> Topic </th>
   </tr>
</thead>
<tbody>


{% include syllabus_entry %}
[//]: <> (lecture 1)
# Introduction and Course Overview
This lecture will be an overview of the class, requirements, and an introduction to the history of machine learning and systems research. 

* Lecture slides: [[pdf](assets/lectures/lec01/01_intro_and_big_ideas_in_ai_systems.pdf), [pptx](assets/lectures/lec01/01_intro_and_big_ideas_in_ai_systems.pptx)]

<div class="reading">

<div class="required_reading" markdown="1">
* [SysML: The New Frontier of Machine Learning Systems](https://arxiv.org/abs/1904.03257)
* Read Chapter 1 of [_Principles of Computer System Design_](https://www.sciencedirect.com/book/9780123749574/principles-of-computer-system-design). You will need to be on campus or use the Library VPN to obtain a free PDF.
* [A Few Useful Things to Know About Machine Learning](https://homes.cs.washington.edu/~pedrod/papers/cacm12.pdf)
</div>

<div class="optional_reading" markdown="1">
* [How to read a paper](https://web.stanford.edu/class/ee384m/Handouts/HowtoReadPaper.pdf) provides some pretty good advice on how to read papers effectively.
* Timothy Roscoe's [writing reviews for systems conferences](https://people.inf.ethz.ch/troscoe/pubs/review-writing.pdf) will also help you in the reviewing process.
</div>
</div>


{% include syllabus_entry %}
[//]: <> (lecture 2)
# Big Data Systems
## [Guest Speaker: Reynold Xin (Databricks)](https://en.wikipedia.org/wiki/Reynold_Xin)

* [Submit your review](https://forms.gle/Arj4xh3NzWWiDbSU7) before 1:00PM.

* Lecture slides: [PDF](assets/lectures/lec02/lec_02.pdf), [PPTX](assets/lectures/lec02/lec_02.pptx)
* Guest Lecture slides: [PDF](assets/lectures/lec02/2022-01-31_Lakehouse_Berkeley.pdf)

<div class="reading">

<div class="required_reading" markdown="1">
* [Towards a Unified Architecture for in-RDBMS Analytics](https://www.cs.stanford.edu/people/chrismre/papers/bismarck.pdf)
* [Resilient Distributed Datasets: A Fault-Tolerant Abstraction for In-Memory Cluster Computing](https://www.usenix.org/system/files/conference/nsdi12/nsdi12-final138.pdf)
* [Lakehouse: A New Generation of Open Platforms that Unify Data Warehousing and Advanced Analytics](http://cidrdb.org/cidr2021/papers/cidr2021_paper17.pdf)
</div>

<div class="optional_reading" markdown="1">
* [Delta Lake: High-Performance ACID Table Storage over Cloud Object Stores](https://databricks.com/wp-content/uploads/2020/08/p975-armbrust.pdf)
* [Spark SQL: Relational Data Processing in Spark](https://people.csail.mit.edu/matei/papers/2015/sigmod_spark_sql.pdf)
* [The MADlib Analytics Library or MAD Skills, the SQL](https://arxiv.org/pdf/1208.4165.pdf)
</div>
</div>

{% include syllabus_entry %}
[//]: <> (lecture 3)
# Hardware for Machine Learning
## [Guest Speaker: Prof. Sophia Shao (UC Berkeley)](https://people.eecs.berkeley.edu/~ysshao/index.html?_ga=2.228137950.2133028827.1643052087-1693328731.1500773369)

* [Submit your review](https://forms.gle/qopNSZp8EuKcDqkT9) before 1:00PM.

* Lecture slides: [PDF](assets/lectures/lec03/lec_03.pdf), [PPTX](assets/lectures/lec03/lec_03.pptx)
* Guest Lecture slides: [PDF](assets/lectures/lec03/shao-ai-sys-guest-lecture-2022.pdf)

<div class="reading">

<div class="required_reading" markdown="1">
* [Mixed precision training. [ICLR’18]](https://openreview.net/pdf?id=r1gs9JgRZ)
* [Eyeriss: A Spatial Architecture for Energy-Efficient Dataflow for Convolutional Neural Networks [SIGRAPH, 2016]](https://dspace.mit.edu/handle/1721.1/102369)
* [Interstellar: Using Halide’s Scheduling Language to Analyze DNN Accelerators (formerly: DNN Dataflow Choice Is Overrated)](https://arxiv.org/pdf/1809.04070.pdf)
* [Gemmini: Enabling Systematic Deep-Learning Architecture Evaluation via Full-Stack Integration [Best Paper Award, DAC’21]](https://people.eecs.berkeley.edu/~ysshao/assets/papers/genc2021-dac.pdf)
</div>

<div class="optional_reading" markdown="1">
* [A New Golden Age for Computer Architecture](https://cacm.acm.org/magazines/2019/2/234352-a-new-golden-age-for-computer-architecture/fulltext)
* [Roofline: An Insightful Visual Performance Model for Floating-Point Programs and Multicore Architectures [CACM’08]](https://people.eecs.berkeley.edu/~kubitron/cs252/handouts/papers/RooflineVyNoYellow.pdf)
</div>
</div>

{% include syllabus_entry %}
[//]: <> (lecture 4)
# Distributed deep learning, Part I: Systems 
## [Guest Speaker: Microsoft DeepSpeed Team](https://www.deepspeed.ai)

* [Submit your review](https://forms.gle/rCsHe1oFqMSiKjgw7) before 1:00PM.

* Lecture slides: [PDF](assets/lectures/lec04/lec_04.pdf), [PPTX](assets/lectures/lec04/lec_04.pptx)
* Guest Lecture slides: [PDF](assets/lectures/lec04/zero-family.pptx)


<div class="reading">

<div class="required_reading" markdown="1">
* [Chimera: Efficiently Training Large-Scale Neural Networks with Bidirectional Pipelines [SC’21, Best Paper finalist]](https://arxiv.org/pdf/2107.06925.pdf)
* [Efficient Large-Scale Language Model Training on GPU Clusters Using Megatron-LM [SC’21, Best Student Paper]](https://arxiv.org/pdf/2104.04473.pdf)
* [ZeRO-Infinity: Breaking the GPU Memory Wall for Extreme Scale Deep Learning [SC’21]](https://arxiv.org/abs/2104.07857)
</div>

<div class="optional_reading" markdown="1">
* [DeepSpeed: Advancing MoE inference and training to power next-generation AI scale [Blog post]](https://www.microsoft.com/en-us/research/blog/deepspeed-advancing-moe-inference-and-training-to-power-next-generation-ai-scale/)
* [Large Scale Distributed Deep Networks [NeurIPS’12]](https://papers.nips.cc/paper/2012/hash/6aca97005c68f1206823815f66102863-Abstract.html)
* [Gpipe: Efficient training of giant neural networks using pipeline parallelism [NeurIPS’19]](https://proceedings.neurips.cc/paper/2019/file/093f65e080a295f8076b1c5722a46aa2-Paper.pdf)
* [PipeDream: Fast and Efficient Pipeline Parallel DNN Training [SOSP'19]](https://arxiv.org/pdf/1806.03377.pdf)
</div>
</div>

{% include syllabus_entry %}
# Holiday (Presidents Day)


{% include syllabus_entry %}
[//]: <> (lecture 6)
# Distributed deep learning, Part II: Scaling Constraints
## [Guest Speaker: Michael Houston (Nvidia)](http://graphics.stanford.edu/~mhouston/)

* [Submit your review](https://forms.gle/Y5ya8YETxwW7jr5aA) before 1:00PM.
* Lecture slides: [PDF](assets/lectures/lec05/lec_05.pdf), [PPTX](assets/lectures/lec05/lec_05.pptx)
* Guest Lecture slides: [PDF](assets/lectures/lec05/UCB_MLSys_Mike_Houston.pdf)

<div class="reading">

<div class="required_reading" markdown="1">
* [Measuring the Effects of Data Parallelism on Neural Network Training](https://arxiv.org/pdf/1811.03600.pdf)
* [Scaling Laws for Neural Language Models [OpenAI, 2020]](https://arxiv.org/pdf/2001.08361.pdf)
* [Deep Learning Training in Facebook Data Centers: Design of Scale-up and Scale-out Systems](https://arxiv.org/abs/2003.09518)
</div>

<div class="optional_reading" markdown="1">
* [On Large-Batch Training for Deep Learning: Generalization Gap and Sharp Minima [ICLR’16]](https://arxiv.org/pdf/1609.04836.pdf)
* [Train Large, Then Compress: Rethinking Model Size for Efficient Training and Inference of Transformers [ICML’20]](https://arxiv.org/pdf/2002.11794.pdf)
* [Large Batch Optimization for Deep Learning: Training BERT in 76 minutes [ICLR’20]](https://arxiv.org/pdf/1904.00962.pdf)
* [Scaling Vision Transformers](https://arxiv.org/pdf/2106.04560.pdf)
</div>
</div>

{% include syllabus_entry %}
[//]: <> (lecture 7)
# Project Proposals 
* Lecture slides: [PDF](assets/lectures/lec06/ml_applied_to_systems.pdf), [PPTX](assets/lectures/lec06/ml_applied_to_systems.pptx)

{% include syllabus_entry %}
[//]: <> (lecture 8)
# Machine learning Applied to Systems
## [Guest Speaker: Prof. Tim Kraska (MIT)](https://www.csail.mit.edu/person/tim-kraska)

* [Submit your review](https://forms.gle/NhtiFZ4GsxYuug3W6) before 1:00PM.
* Lecture slides: [PDF], [PPTX]

<div class="reading">

<div class="required_reading" markdown="1">
* [The Case for Learned Index Structures [ICMD’18]](https://arxiv.org/abs/1712.01208)
* [Device Placement Optimization with Reinforcement Learning [ICML’17]](https://arxiv.org/pdf/1706.04972.pdf)
* [Neural Adaptive Video Streaming with Pensieve [SIGCOMM’17]](https://people.csail.mit.edu/hongzi/content/publications/Pensieve-Sigcomm17.pdf)
</div>

</div>

{% include syllabus_entry %}
# Spring Break

{% include syllabus_entry %}
[//]: <> (lecture 10)
# Machine Learning Frameworks and Automatic Differentiation
## [Guest Speaker: Prof. Tianqi Chen (OctoML and CMU)](https://tqchen.com)

* [Submit your review](https://forms.gle/sxMrFsWDGsrToaxm6) before 1:00PM.
* Lecture slides: [PDF](assets/lectures/lec10/lec10.pdf), [PPTX](assets/lectures/lec10/lec10.pptx)
* Joey's Lecture slides: [PDF](assets/lectures/lec10/10_deep_learning_frameworks.pdf), [PPTX](assets/lectures/lec10/10_deep_learning_frameworks.pptx)

<div class="reading">

<div class="required_reading" markdown="1">
* [Automatic differentiation in ML: Where we are and where we should be going](https://papers.nips.cc/paper/8092-automatic-differentiation-in-ml-where-we-are-and-where-we-should-be-going)
* [TensorFlow: A System for Large-Scale Machine Learning](https://www.usenix.org/system/files/conference/osdi16/osdi16-abadi.pdf)
* [TVM: An Automated End-to-End Optimizing Compiler for Deep Learning](https://arxiv.org/abs/1802.04799)
</div>

</div>


{% include syllabus_entry %}
[//]: <> (lecture 11)
# Efficient Machine Learning
## [Guest Speaker: Vikas Chandra (Facebook)](https://www.linkedin.com/in/vchandra/)

* [Submit your review](https://forms.gle/gXiLKSUEuFLscZuS9) before 1:00PM.
* Lecture slides: [PDF](assets/lectures/lec11/cloud_computing_for_ml_sys_class.pdf), [PPTX](assets/lectures/lec11/cloud_computing_for_ml_sys_class.pptx)

<div class="reading">
<div class="required_reading" markdown="1">
* [Linear Mode Connectivity and the Lottery Ticket Hypothesis](https://arxiv.org/pdf/1912.05671.pdf)
* [Integer-only Quantization of Neural Networks for Efficient Integer-Arithmetic-Only Inference](https://arxiv.org/pdf/1712.05877.pdf)
* [FBNet: Hardware-Aware Efficient ConvNet Design via Differentiable Neural Architecture Search](https://arxiv.org/abs/1812.03443)
</div>

<div class="optional_reading" markdown="1">
* [Hessian Aware trace-Weighted Quantization of Neural Networks](https://proceedings.neurips.cc/paper/2020/file/d77c703536718b95308130ff2e5cf9ee-Paper.pdf)
* [The state of sparsity in deep neural networks](https://arxiv.org/pdf/1902.09574.pdf)
* [Sparsity in Deep Learning: Pruning and growth for efficient inference and training in neural networks](https://arxiv.org/pdf/2102.00554.pdf)
</div>
</div>


{% include syllabus_entry %}
[//]: <> (lecture 12)
# Fundamentals of Machine Learning in the Cloud, the Modern Data Stack  
## [Guest Speaker: Prof. Matei Zaharia (Databricks and Stanford)](https://cs.stanford.edu/people/matei/)

* [Submit your review](https://forms.gle/qY7cgn4eAuutJQoz8) before 1:00PM.
* Lecture slides: [PDF], [PPTX]

<div class="reading">
<div class="required_reading" markdown="1">
* [The Sky Above The Clouds](https://drive.google.com/file/d/16xs_-3XRym34z60-Ji4dlDwW487vOmpz/view?usp=sharing)
* [FrugalML: How to Use ML Prediction APIs More Accurately and Cheaply](https://arxiv.org/abs/2006.07512)
* [Pollux: Co-adaptive Cluster Scheduling for Goodput-Optimized Deep Learning](https://www.usenix.org/system/files/osdi21-qiao.pdf)
</div>
<div class="optional_reading" markdown="1">
* [RubberBand: cloud-based hyperparameter tuning](https://dl.acm.org/doi/10.1145/3447786.3456245)
</div>
</div>


{% include syllabus_entry %}
[//]: <> (lecture 13)
# Benchmarking Machine Learning Workloads
## [Guest Speaker: Prof. Vijay Reddi (Harvard)](https://scholar.harvard.edu/vijay-janapa-reddi/home)

* Lecture slides: [PDF], [PPTX]

<div class="reading">

<div class="required_reading" markdown="1">
* [MLPerf Training Benchmark](https://proceedings.mlsys.org/paper/2020/hash/02522a2b2726fb0a03bb19f2d8d9524d-Abstract.html)
* [MLPerf Inference Benchmark](https://arxiv.org/pdf/1911.02549.pdf)
* [Benchmark Analysis of Representative Deep Neural Network Architectures](https://arxiv.org/pdf/1810.00736.pdf)
</div>

</div>

{% include syllabus_entry %}
[//]: <> (lecture 14)
# Machine learning and Security

* Lecture slides: [PDF], [PPTX]

<div class="reading">
<div class="required_reading" markdown="1">

* [Communication-Efficient Learning of Deep Networks from Decentralized Data](https://arxiv.org/pdf/1602.05629.pdf)
* [Privacy Accounting and Quality Control in the Sage Differentially Private ML Platform](https://arxiv.org/pdf/1909.01502.pdf)  
* [Slalom: Fast, Verifiable and Private Execution of Neural Networks in Trusted Hardware](https://arxiv.org/abs/1806.03287)

</div>
<div class="optional_reading" markdown="1">

* [Helen: Maliciously Secure Coopetitive Learning for Linear Models](https://people.eecs.berkeley.edu/~wzheng/helen_ieeesp.pdf)
* [Faster CryptoNets: Leveraging Sparsity for Real-World Encrypted Inference](https://arxiv.org/abs/1811.09953)
* [Rendered Insecure: GPU Side Channel Attacks are Practical](https://www.cs.ucr.edu/~zhiyunq/pub/ccs18_gpu_side_channel.pdf)
* [The Algorithmic Foundations of Differential Privacy](https://www.cis.upenn.edu/~aaroth/Papers/privacybook.pdf)
* [Federated Learning: Collaborative Machine Learning without Centralized Training Data](https://ai.googleblog.com/2017/04/federated-learning-collaborative.html)
* [Federated Learning at Google ... A comic strip?](https://federated.withgoogle.com)
* [SecureML: A System for Scalable Privacy-Preserving Machine Learning](https://eprint.iacr.org/2017/396.pdf)
* More reading coming soon ...
</div>
</div>


{% include syllabus_entry %}
# RRR Week

{% include syllabus_entry %}
# Project Presentations


</td>
</tr>
</tbody>
</table>

## Projects

Detailed candidate project descriptions will be posted shortly.  However, students are encourage to find projects that relate to their ongoing research.


## Grading

Grades will be largely based on class participation and projects.  In addition, we will require weekly paper summaries submitted before class.
* **Projects:** _60%_
* **Weekly Summaries:** _20%_
* **Class Participation:** _20%_









<script type="text/javascript">


var current_date = new Date();
var rows = document.getElementsByTagName("th");
var finished =  false;
for (var i = 1; i < rows.length && !finished; i++) {
   var r = rows[i];
   if (r.id.startsWith("counter_")) {
      var fields = r.id.split("_")
      var week_div_id = "week_" + fields[2]
      var lecture_date = new Date(fields[1] + " 23:59:00")
      if (current_date <= lecture_date) {
         finished = true;
         r.style.background = "orange"
         r.style.color = "black"
         var week_td = document.getElementById(week_div_id)
         week_td.style.background = "#043361"
         week_td.style.color = "white"
         var anchor = document.createElement("div")
         anchor.setAttribute("id", "today")
         week_td.prepend(anchor)
      }
   }
}

$(".reading").each(function(ind, elem) {
   var optional_reading = $(elem).find(".optional_reading");
   if(optional_reading.length == 1) {
      optional_reading = optional_reading[0];
      optional_reading.setAttribute("id", "optional_reading_" + ind);
      var button = document.createElement("button");
      button.setAttribute("class", "btn btn-primary btn-sm");
      button.setAttribute("type", "button");
      button.setAttribute("data-toggle", "collapse");
      button.setAttribute("data-target", "#optional_reading_" + ind);
      button.setAttribute("aria-expanded", "false");
      button.setAttribute("aria-controls", "#optional_reading_" + ind);
      optional_reading.setAttribute("class", "optional_reading_no_heading collapse")
      button.innerHTML = "Additional Optional Reading";
      optional_reading.before(button)
   }
   
})


$(".details").each(function(ind, elem) {
      elem.setAttribute("id", "details_" + ind);
      var button = document.createElement("button");
      button.setAttribute("class", "btn btn-primary btn-sm");
      button.setAttribute("type", "button");
      button.setAttribute("data-toggle", "collapse");
      button.setAttribute("data-target", "#details_" + ind);
      button.setAttribute("aria-expanded", "false");
      button.setAttribute("aria-controls", "#details_" + ind);
      elem.setAttribute("class", "details_no_heading collapse")
      button.innerHTML = "Detailed Description";
      elem.before(button)
   })

</script>


