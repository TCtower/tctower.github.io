---
layout: single
author_profile: true
toc: false
toc_label: "Contents"
toc_icon: "cog"

---
<style type="text/css">

body{ /* Normal  */
      font-size: 17px;
  }

.author__avatar{
    padding-left:10%;
    padding-right:10%;
}

.author__content{
    text-align: center;

}

.author__avatar img{
    max-width:100%;
}

.author__urls{
    padding-left: 15%;
}

.page__content p {
    margin-top: 1.5em;
    margin-bottom: 1.5em;
}

.page{
    padding-right: 0%;
    font-size: 15px;
}

strong {
    color: #616161;
}

.news-item {
    display: list-item;
}

.news-item.hidden {
    display: none;
}

#expand-news-link,
.read-more-link {
    cursor: pointer;
    text-decoration: none;
}

#expand-news-link:hover,
.read-more-link:hover {
    text-decoration: underline;
}
</style>

Welcome to my homepage!

<!-- <br />  -->

I’m a third-year PhD student in [Computer Science and Engineering](https://www.cse.umich.edu/) at [University of Michigan, Ann Arbor](https://www.umich.edu/), advised by [Prof. Mosharaf Chowdhury](https://www.mosharaf.com/). My current research interests involve <em>Agentic AI Systems</em>, <em>Multimodal Model Training</em> and <em>Distributed Machine Learning</em>. 

Before UMich, I completed my MSc in Computer Science at [University of British Columbia](https://www.ubc.ca/), working with [Prof. Ivan Beschastnikh](https://www.cs.ubc.ca/~bestchai/) and [Prof. Mathias Lécuyer](http://mathias.lecuyer.me/). I obtained my Bachelor’s in Computing at [Hong Kong Polytechnic University](https://www.polyu.edu.hk/en/), under the supervision of [Prof. Song Guo](https://cse.hkust.edu.hk/~songguo/).


<!-- Prior to this, in my MSc work, I proposed [GlueFL](https://arxiv.org/abs/2212.01523), a federated learning framework designed to optimize downstream bandwidth. Even before, I did an internship at [Microsoft Research Asia (MSRA)](https://www.microsoft.com/en-us/research/lab/microsoft-research-asia/), working with [Dr. Yang Chen](https://www.microsoft.com/en-us/research/people/yachen/). We worked on [Forerunner](https://www.microsoft.com/en-us/research/uploads/prod/2021/09/3477132.3483564.pdf), a novel computing framework that leverages speculative execution to accelerate transaction processing on [Ethereum](https://ethereum.org/en/). -->

<!-- I love solving algorithm problems. In past years, I participated in a number of programming contests, such as [ACM ICPC Regional Contest](https://icpc.global/), [IEEEXtreme](https://ieeextreme.org/), and [National Olympiad in Informatics in Province](https://www.noi.cn/). I am also an experienced codeforces [user](https://codeforces.com/profile/TCtower) :). -->

<!-- # Heading
sss -->

## News
<ul id="news-list">
<li class="news-item">
<strong>2026-01</strong> - <a href="https://arxiv.org/pdf/2502.00241" title="mordal">Mordal</a> has been accepted to ICLR 2026.
</li>
<li class="news-item">
<strong>2026-01</strong> - <a href="https://arxiv.org/pdf/2510.01565" title="tetriserve">TetriServe</a> has been accepted to ASPLOS 2026.
</li>
<li class="news-item">
<strong>2025-06</strong> - Work as a research intern at Alibaba Tongyi Lab.
<br/><a href="hhttps://github.com/agentscope-ai/agentscope/" title="c4"> AgentScope 1.0: A Developer-Centric Framework for Building Agentic Applications </a>
</li>
<li class="news-item">
<strong>2024-12</strong> - <a href="https://www.cs.ubc.ca/~bestchai/papers/infocom25-fedfetch.pdf">FedFetch</a> has been accepted to INFOCOM 2025.
</li>
<li class="news-item">
<strong>2024-05</strong> - <a href="https://www.usenix.org/system/files/usenixsecurity24-jiang-zhifeng.pdf" title="c4">Lotto</a> has been accepted to USENIX Security 2024.
</li>
<li class="news-item">
<strong>2023-09</strong> - Starting my PhD at UMich!
</li>
<li class="news-item">
<strong>2023-06</strong> - Work as a research assistant at HKUST, under the supervision of <a href="https://www.cse.ust.hk/~weiwa/" title="c4">Prof. Wei Wang</a>.
</li>
<li class="news-item">
<strong>2023-05</strong> - <a href="https://arxiv.org/pdf/2206.05891.pdf" title="c4">FedAMD</a> has been accepted to ICML 2023.
</li>
<li class="news-item hidden">
<strong>2023-02</strong> - <a href="https://arxiv.org/pdf/2212.01523.pdf" title="c4">GlueFL</a> has been accepted to MLSys 2023.
</li>
<li class="news-item hidden">
<strong>2022-07</strong> - Join our competition at NeurIPS 2022! 
<br/><a href="https://nl4opt.github.io/" title="c4"> NL4Opt: Formulating Optimization Problems Based on Their Natural Language Descriptions </a>
</li>
</ul>
<p style="text-align: right; margin-top: 1em;">
  <a id="expand-news-link" onclick="toggleNews()">Expand to show all news →</a>
</p>

<script>
function toggleNews() {
    const hiddenItems = document.querySelectorAll('.news-item.hidden');
    const expandLink = document.getElementById('expand-news-link');
    
    if (hiddenItems.length > 0) {
        // Expand: show all items
        hiddenItems.forEach(item => {
            item.classList.remove('hidden');
        });
        expandLink.textContent = 'Show less ←';
    } else {
        // Collapse: hide items beyond first 5
        const allItems = document.querySelectorAll('.news-item');
        allItems.forEach((item, index) => {
            if (index >= 5) {
                item.classList.add('hidden');
            }
        });
        expandLink.textContent = 'Expand to show all news →';
    }
}

// Initialize: hide items beyond first 5 on page load
document.addEventListener('DOMContentLoaded', function() {
    const allItems = document.querySelectorAll('.news-item');
    allItems.forEach((item, index) => {
        if (index >= 5) {
            item.classList.add('hidden');
        }
    });
});
</script>

## Selected Publications & Preprints
<ul>
<!-- <em style="color:#cc6600;">Submitted</em> -->
<!-- <em style="color:seagreen;">To appear</em> -->


<li>
<strong>Branch-and-Browse: Efficient and Controllable Web Exploration with Tree-Structured Reasoning and Action Memory
</strong>
<br/><u><em>Shiqi He</em></U>, Yue Cui, Xinyu Ma, Yaliang Li, Bolin Ding, Mosharaf Chowdhury
<br/> <em style="color:#800017;"> arXiv Preprint </em>  [<a href="https://arxiv.org/pdf/2510.19838" title="p4">.pdf</a>] 
</li>

<li>
<strong>TetriServe: Efficient DiT Serving for Heterogeneous Image Generation</strong>
<br/>Runyu Lu*, <u><em>Shiqi He*</em></U>, Wenxuan Tan, Shenggui Li, Ruofan Wu, Jeff J. Ma, Ang Chen, Mosharaf Chowdhury
<br/> <em style="color:#800017;"> ASPLOS 2026 </em>  [<a href="https://arxiv.org/pdf/2510.01565" title="p4">.pdf</a>] 
</li>

<li>
<strong>Mordal: Automated Pretrained Model Selection for Vision Language Models</strong>
<br/><u><em>Shiqi He</em></U>, Insu Jang, Mosharaf Chowdhury
<br/> <em style="color:#800017;"> ICLR 2026 </em>  [<a href="https://arxiv.org/pdf/2502.00241" title="p4">.pdf</a>] 
</li>

<!-- <li>
<strong>FedFetch: Faster Federated Learning with Adaptive Downstream Prefetching</strong>
<br/>Qifan Yan, Andrew Liu, <u><em>Shiqi He</em></U>, Mathias Lecuyer, Ivan Beschastnikh
<br/> <em style="color:#800017;"> INFOCOM 2025 </em>  
</li> -->
  
<li>
<strong>Lotto: Secure Participant Selection against Adversarial Servers in Federated Learning</strong>
<br/>Zhifeng Jiang, Peng Ye, <u><em>Shiqi He</em></U>, Wei Wang, Ruichuan Chen, Bo Li
<br/> <em style="color:#800017;"> USENIX Security 2024 </em>  [<a href="https://www.usenix.org/system/files/usenixsecurity24-jiang-zhifeng.pdf" title="p4">.pdf</a>] 
</li>


<!-- <li>
<strong>Anchor Sampling for Federated Learning with Partial Client Participation</strong>
<br/>Feijie Wu, Song Guo, Zhihao Qu, <u><em>Shiqi He</em></U>, Ziming Liu, Jing Gao
<br/> <em style="color:#800017;"> International Conference on Machine Learning (ICML 2023) </em>  [<a href="https://arxiv.org/pdf/2206.05891.pdf" title="p4">.pdf</a>] 
</li> -->

<li>
<strong>GlueFL: Reconciling Client Sampling and Model Masking for Bandwidth Efficient Federated Learning</strong>
<br/><u><em>Shiqi He</em></U>, Qifan Yan, Feijie Wu, Lanjun Wang, Mathias Lécuyer, Ivan Beschastnikh 
<br/> <em style="color:#800017;"> MLSys 2023 </em> [<a href="https://arxiv.org/pdf/2212.01523.pdf" title="p4">.pdf</a>]
</li>

<li>
<strong>NL4Opt Competition: Formulating Optimization Problems Based on Their Natural Language Descriptions</strong>
<br/>Rindranirina Ramamonjison, Timothy Yu, Raymond Li, Haley Li, Giuseppe Carenini, Bissan Ghaddar, <u><em>Shiqi He</em></U>, Mahdi Mostajabdaveh, Amin Banitalebi-Dehkordi, Zirui Zhou, Yong Zhang
<br/> <em style="color:#800017;"> NeurIPS 2022 Competitions </em> [<a href="https://arxiv.org/pdf/2209.15565.pdf" title="p3">.pdf</a>]
</li>

<!-- <li>
<strong>Sign Bit is Enough: A Learning Synchronization Framework for Multi-hop All-reduce with Ultimate Compression</strong>
<br/>Feijie Wu*, <u><em>Shiqi He*</em></U>, Song Guo, Zhihao Qu, Haozhao Wang, Weihua Zhuang, Jie Zhang
<br/> <em style="color:#800017;"> Design Automation Conference (DAC 2022) </em> [<a href="https://arxiv.org/pdf/2204.06787.pdf" title="p2">.pdf</a>]
</li> -->


<p style="text-align: right; margin-top: 1em;">
  <a href="https://scholar.google.com/citations?user=9eYlWYAAAAAJ&hl=en" target="_blank" class="read-more-link">Read more on Google Scholar →</a>
</p>


<!-- 
<li>
<strong>On the Convergence of Quantized Parallel Restarted SGD for Serverless Learning</strong>
<br/>Feijie Wu, <u><em>Shiqi He</em></U>, Yutong Yang, Haozhao Wang, Zhihao Qu, Song Guo
<br/> arXiv, preprint arXiv:2004.09125. [<a href="https://arxiv.org/pdf/2004.09125.pdf" title="p1">.pdf</a>] 
</li>
</ul> -->

<!-- Lafuente, E., <u><strong>Lürig, M.D.</strong></u>, Rövekamp, M., Matthews, B., Buser, C., Vorburger, C., and Räsänen, K.. Building on 150 years of knowledge: the freshwater isopod <i>Asellus aquaticus</i> as an integrative eco-evolutionary model system. Frontiers in Ecology and Evolution. <i>In press</i>. -->

<!-- 
<h1>{{ "Recent Publication" | toc .toc__menu }}</h1>
sdasdasd

<h2>{{ "Recent Publication" | toc__menu}}</h2>

sdsasas -->
