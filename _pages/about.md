---
permalink: /
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---
<style>
    #news,
    #experience,
    #publications,
    #projects,
    #awards,
    #talks {
        scroll-margin-top: 80px;
    }
  
      /* ===== News Scroll Box ===== */
    .news-box {
      max-height: 220px;
      overflow-y: auto;
      padding: 10px 14px;
      background: #f7f7f7;
      border-radius: 10px;
      margin-bottom: 20px;
    }
    
    .news-list {
      list-style: none;
      padding: 0;
      margin: 0;
    }
    
    .news-list li {
      margin-bottom: 10px;
      line-height: 1.5;
    }
    
    .news-date {
      display: inline-block;
      min-width: 70px;
      font-weight: 400;        /* 不加粗 */
      color: #ca6f6f;          /* 浅粉色 */
    }
  
    .experience-card {
        display: flex;
        align-items: center;
        background: #f9f9f9;
        border-radius: 12px;
        padding: 16px;
        margin-bottom: 0px;
        box-shadow: 0 4px 8px rgba(0,0,0,0.05);
        transition: transform 0.3s, box-shadow 0.3s;
    }
    .experience-card:hover {
       
        box-shadow: 0 8px 16px rgba(0,0,0,0.1);
    }
    .experience-logo {
        width: 60px;
        height: 60px;
        margin-right: 20px;
        border-radius: 8px;
        object-fit: contain;
    }
    .experience-info {
        font-family: "Segoe UI", sans-serif;
    }
    .experience-info strong {
        font-size: 1.1em;
    }
    .experience-info a {
        text-decoration: none;
        color: #ca6f6f;
    }
    .experience-container {
        display: flex;
        flex-direction: column; /* 让子元素垂直排列，一行一个 */
        gap: 20px; /* 保持每个卡片之间的间距 */
    }
    .experience-card {
        box-sizing: border-box;
    }
    .publication-card {
        display: flex;
        align-items: center;
        padding: 3px;
        border: 1.5px solid #ddd;
        border-radius: 8px;
        background: #fff;
        box-sizing: border-box;
        margin-bottom: 20px; 
        transition: transform 0.3s ease, box-shadow 0.3s ease;

        color: #5f6368; /* 正文整体更浅 */
    }
    .publication-card > div > strong,
    .publication-card > div > div > strong {
        color: #202124;
    }
    .publication-card i {
        color: #6b7280;
    }

    .pub-badge {
        display: inline-flex;
        align-items: center;
        gap: 0.35em;
        margin-left: 8px;
        padding: 2px 8px;
        border-radius: 999px;
        font-size: 11px;
        font-weight: 650;
        line-height: 1.4;
        letter-spacing: 0.01em;
        vertical-align: middle;
        white-space: nowrap;
        border: 1px solid transparent;
        background: rgba(107, 114, 128, 0.08);
        color: #6b7280;
    }

    .pub-badge::before {
        content: "";
        width: 0.45em;
        height: 0.45em;
        border-radius: 999px;
        background: currentColor;
        opacity: 0.75;
    }

    .pub-badge--oral {
        margin-left: 4px;
        vertical-align: 2px;
        color: #4c6a94;
        background: rgba(131, 161, 199, 0.14);
        border-color: rgba(131, 161, 199, 0.35);
    }
    .publication-card:hover {
       
        box-shadow: 0 8px 16px rgba(0,0,0,0.1);
    }

    .publication-card.featured {
        border-color: #f5bba7;       /* 更浅的哈密瓜色边框 */
        background: #fef5f1;         /* 非常浅的哈密瓜色背景 */
        box-shadow: 0 4px 8px rgba(242, 166, 120, 0.2); /* 更柔和的初始阴影 */
        z-index: 10;
    }

    .publication-card.featured:hover {
        box-shadow: 0 8px 16px rgba(242, 166, 120, 0.4); 
    }
    
    /*.publication-card.non-featured {*/
        /*display: flex;  默认隐藏非精选出版物 */
    /*}*/
    
    .pub-button-container {
        display: flex;
        gap: 10px;
        margin: 20px 0;
        flex-wrap: wrap;
    }
    
    .pub-button {
        background-color: #f0f0f0;
        border: 1px solid #ccc;
        border-radius: 20px;
        padding: 8px 16px;
        cursor: pointer;
        transition: all 0.3s ease;
    }
    
    .pub-button:hover {
        background-color: #e0e0e0;
    }
    
    .pub-button.active {
        background-color: #ca6f6f;
        color: white;
        border-color: #ca6f6f;
    }

      .publication-view[hidden] {
        display: none !important;
    }

      #full-publications {
        max-height: 380px;
        overflow-y: auto;
        padding-right: 8px;
        margin-bottom: 24px;
        scroll-behavior: smooth;
        scrollbar-width: thin;
        scrollbar-color: rgba(185, 95, 61, 0.45) rgba(254, 245, 241, 0.7);
    }

    #full-publications::-webkit-scrollbar {
        width: 8px;
    }

    #full-publications::-webkit-scrollbar-track {
        background: rgba(254, 245, 241, 0.7);
        border-radius: 999px;
    }

    #full-publications::-webkit-scrollbar-thumb {
        background: rgba(185, 95, 61, 0.45);
        border-radius: 999px;
    }

    #full-publications::-webkit-scrollbar-thumb:hover {
        background: rgba(185, 95, 61, 0.65);
    }
  
    .full-publication-list {
        margin: 0;
        padding-left: 1.25rem;
        color: #5f6368;
        font-size: 15px;
        line-height: 1.55;
    }

    .full-publication-list li {
        margin-bottom: 14px;
    }

    .pub-list-badge {
        display: inline-block;
        margin-right: 6px;
        padding: 2px 8px;
        border-radius: 999px;
        border: 1px solid rgba(245, 187, 167, 0.75);
        background: #fef5f1;
        color: #b95f3d;
        font-size: 11px;
        font-weight: 650;
        line-height: 1.35;
        vertical-align: 1px;
        white-space: nowrap;
    }

    .full-publication-list .pub-list-title {
        color: #202124;
        font-size: 15px;
        font-weight: 700;
        line-height: 1.45;
        text-decoration: none !important;
    }

      .pub-list-authors {
        color: #6b7280;
        font-size: 13px;
        font-style: italic;
    }

    .pub-list-authors > strong {
        color: #202124;
    }

      .pub-list-authors a strong {
        color: inherit;
    }

    .pub-list-note {
        color: #c7774c;
        font-style: italic;
        font-weight: 650;
    }

    .pub-list-links {
        white-space: nowrap;
    }

    .pub-list-links a {
        margin-left: 4px;
        color: #c7774c !important;
        font-weight: 600;
    }

      .pub-list-links a:hover {
        color: #b65f36 !important;
    }

    /* Projects cards: keep styles independent from publications */
    .project-card {
        display: flex;
        align-items: center;
        padding: 3px;
        border: 1.5px solid #ddd;
        border-radius: 8px;
        background: #fff;
        box-sizing: border-box;
        margin-bottom: 20px;
        transition: transform 0.3s ease, box-shadow 0.3s ease;

        color: #5f6368;
    }

    .project-card > div > strong,
    .project-card > div > div > strong {
        color: #202124;
    }

    .project-card i {
        color: #6b7280;
    }

    .project-card:hover {
        box-shadow: 0 8px 16px rgba(0,0,0,0.1);
    }

      @media (max-width: 720px) {
        .publication-card,
        .project-card {
            align-items: stretch;
            padding: 8px;
        }

        .publication-card > div,
        .project-card > div {
            flex-direction: column;
            align-items: stretch !important;
            width: 100%;
        }

        .publication-card .pub-media-rotator,
        .project-card .pub-media-rotator {
            width: 100% !important;
            height: auto !important;
            aspect-ratio: 16 / 9;
            margin-right: 0 !important;
            margin-bottom: 12px;
        }

        .publication-card .pub-media-rotator > img,
        .project-card .pub-media-rotator > img {
            width: 100% !important;
            height: 100% !important;
            object-fit: contain;
        }

        .publication-card strong,
        .project-card strong {
            line-height: 1.35;
        }

        .full-publication-list {
            padding-left: 1rem;
        }

        .pub-list-badge {
            margin-bottom: 4px;
        }
    }

  
</style>
<html> 
<head>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Permanent+Marker&display=swap');
        @import url('https://fonts.googleapis.com/css2?family=Fredericka+the+Great&display=swap');
        @import url('https://fonts.googleapis.com/css2?family=Homemade+Apple&display=swap');
        body {
            background-color:	 #FFFFFF;
            font-family: 'Arial Rounded MT Bold', 'Verdana', sans-serif;
            font-size: 15px;
        }
        .main-heading {
            font-family: 'Permanent Marker', cursive;
            text-align: center;
            color: #ca6f6f;
        }
        div.markdown-body a,a {
            text-decoration: none !important;
            color: #ca6f6f;
            transition: all 0.3s ease; /* 平滑过渡效果 */
        }
        div.markdown-body a:hover, a:hover {
            color: #c71585;            /* 悬浮时变深一点的颜色 */
            text-decoration: underline; /* 加上悬浮时的下划线 */
        }
    </style>
</head>
<body>
<h1 class="main-heading">Hi there <img src="images/Hi.gif" width="40px"> Welcome to my Homepage!</h1>
</body>
</html>

Hi! I am a  3rd-year PhD. student at Peking University. 

My research interests include **Embodied AI**, **3D/4D Reconstruction**, **Digital Human** and other emerging areas in AI. I enjoy exploring diverse research directions and collaborating with researchers across different fields.

Feel free to reach out if you are interested in collaboration or potential opportunities.

Main News
---------------
<div class="news-box">
  <ul class="news-list">
    <li><span class="news-date"><em>2026.04</em></span> 🎉🎉 Two papers accepted to SIGGRAPH 2026 (1 conferecne, 1 journal).</li>
    <li><span class="news-date"><em>2026.02</em></span> 🎉🎉 Two paper accepted to CVPR 2026.</li>
    <li><span class="news-date"><em>2025.07</em></span> 🎉🎉 One paper accepted to ICCV 2025.</li>
    <li><span class="news-date"><em>2025.01</em></span> 🎉🎉 One paper accepted to ICLR 2025.</li>
  </ul>
</div>

Experience
--------------

<div class="experience-container">
<div class="experience-card">
      <img src="images/pku.png" alt="pku logo" class="experience-logo">
      <div class="experience-info">
          <strong>Peking University</strong><br>
          <em>2023.09 - Present</em><br>
          Ph.D. Student, advised by Prof. Ronggang Wang
      </div>
  </div> 


  
  <div class="experience-card">
      <img src="images/hit.svg" alt="hit logo" class="experience-logo">
      <div class="experience-info">
          <strong>Harbin Institute of Technology</strong><br>
          <em>2019.9 - 2023.7</em><br>
          B.Eng. in Computer Science
      </div>
  </div>
  
</div>


Publications
--------------
<button class="pub-button active" onclick="filterPublications(event, 'all')">Core Publications</button>
<button class="pub-button" onclick="filterPublications(event, 'list')">Full Publications List</button>

(* equal contribution · ✉ corresponding author)

<div id="core-publications" class="publication-view" data-publication-view="core">

<div class="publication-card" data-category="all"> 
  <div style="display: flex; align-items: center;">
    <div class="pub-media-rotator" data-interval="4000" style="position: relative; width: 320px; height: 180px; margin-right: 20px; border-radius: 8px; overflow: hidden; flex: 0 0 auto;"> 
      <img src="images/atgs.png" alt="wog" style="width: 320px; height: 180px; object-fit: contain; display: block; margin: 0 auto;"> 
    </div> 
    <div>
      <strong>ATGS: Anchored Temporal Gaussian Splatting for Long Volumetric Video Representation</strong><br>
      <i style="font-size: 13px;">
        <a href="https://wujh2001.github.io" target="_blank"><strong>Jiahao Wu*</strong></a>, 
        Jie Liang*, 
        Die Hu, 
        Jiayu Yang, 
        Kaiqiang Xiong, 
        Xiaoyun Zheng, 
        Xiang Li, 
        Chao Wang ✉, 
        Ronggang Wang ✉
      </i><br> 
      Revealing the mechanisms of long-sequence, complex volumetric video reconstruction.
      <br> 
      <b><i style="color:#83a1c7;">ACM TRANSACTIONS ON GRAPHICS [SIGGRAPH'2026] &nbsp;
      </i></b> 
      <a href=""><em>[arXiv]</em></a> 
      <a href="https://github.com/WuJH2001/ATGS"><em>[code]</em></a> 
      <a href="https://wujh2001.github.io/ATGS/"><em>[Project page]</em></a> 
    </div>
  </div> 
</div>


<div class="publication-card" data-category="all"> 
  <div style="display: flex; align-items: center;">
    <div class="pub-media-rotator" data-interval="4000" style="position: relative; width: 320px; height: 180px; margin-right: 20px; border-radius: 8px; overflow: hidden; flex: 0 0 auto;"> 
      <img src="images/clipgstream.png" alt="wog" style="width: 320px; height: 180px; object-fit: contain; display: block; margin: 0 auto;"> 
    </div> 
    <div>
      <strong>ClipGStream: Clip-Stream Gaussian Splatting for Any Length and Any Motion Multi-View Dynamic Scene Reconstruction</strong><br>
      <i style="font-size: 13px;">
      Jie Liang*, 
       <a href="https://wujh2001.github.io" target="_blank"><strong>Jiahao Wu*</strong></a>, 
      Chao Wang, Jiayu Yang, Xiaoyun Zheng, Kaiqiang Xiong, Zhanke Wang, Jinbo
      Yan, FengGao, Ronggang Wang
      </i><br> 
      A streaming dynamic reconstruction strategy based on fragment-wise training.
      <br> 
      <b><i style="color:#83a1c7;">Conference on Computer Vision and Pattern Recognition (CVPR), 2026 &nbsp;
      </i></b> 
      <a href="https://arxiv.org/abs/2604.13746"><em>[arXiv]</em></a> 
      <a href="https://liangjie1999.github.io/ClipGStreamWeb/"><em>[Project page]</em></a> 
    </div>
  </div> 
</div>


<div class="publication-card" data-category="all"> 
  <div style="display: flex; align-items: center;">
    <div class="pub-media-rotator" data-interval="4000" style="position: relative; width: 320px; height: 180px; margin-right: 20px; border-radius: 8px; overflow: hidden; flex: 0 0 auto;"> 
      <img src="images/localdygs.png" alt="wog" style="width: 320px; height: 180px; object-fit: contain; display: block; margin: 0 auto;"> 
    </div> 
    <div>
      <strong>LocalDyGS: Multi-view Global Dynamic Scene Modeling through Adaptive Local Feature Decoupling.</strong><br>
      <i style="font-size: 13px;">
        <a href="https://wujh2001.github.io" target="_blank"><strong>Jiahao Wu</strong></a>, 
        Rui Peng, Jianbo Jiao, Jiayu Yang, Luyang Tang, Kaiqiang Xiong, Jie Liang, Jinbo Yan, Runling Liu, Ronggang Wang
      </i><br> 
      Extend dynamic reconstruction from small-scale motions to complex motions in large-scale scenes.
      <br> 
      <b><i style="color:#83a1c7;">International Conference on Computer Vision (ICCV), 2025 &nbsp;
      </i></b> 
      <a href="https://arxiv.org/pdf/2507.02363"><em>[arXiv]</em></a> 
      <a href="https://github.com/WuJH2001/LocalDyGS"><em>[code]</em></a> 
      <a href="https://wujh2001.github.io/LocalDyGS/"><em>[Project page]</em></a> 
    </div>
  </div> 
</div>


<div class="publication-card" data-category="all"> 
  <div style="display: flex; align-items: center;">
    <div class="pub-media-rotator" data-interval="4000" style="position: relative; width: 320px; height: 180px; margin-right: 20px; border-radius: 8px; overflow: hidden; flex: 0 0 auto;"> 
      <img src="images/swift4d.png" alt="wog" style="width: 320px; height: 180px; object-fit: contain; display: block; margin: 0 auto;"> 
    </div> 
    <div>
      <strong>Swift4D: Adaptive Divide-and-Conquer Gaussian Splatting for Compact and Efficient Reconstruction of Dynamic Scenes.</strong><br>
      <i style="font-size: 13px;">
      <a href="https://wujh2001.github.io" target="_blank"><strong>Jiahao Wu</strong></a>, 
      Rui Peng, Zhiyan Wang, Lu Xiao, Luyang Tang, Kaiqiang Xiong, Ronggang Wang
      </i><br> 
      Achieve fast dynamic reconstruction through motion–static decoupling.
      <br> 
      <b><i style="color:#83a1c7;">International Conference on Learning Representations (ICLR), 2025 &nbsp;
      </i></b> 
      <a href="https://arxiv.org/abs/2503.12307"><em>[arXiv]</em></a> 
      <a href="https://github.com/WuJH2001/Swift4d"><em>[code]</em></a> 
    </div>
  </div> 
</div>

</div>
<div id="full-publications" class="publication-view" data-publication-view="list" hidden>
  <ul class="full-publication-list">
    <li>
      <span class="pub-list-badge">T-CSVT 2026</span>
      <span class="pub-list-title">i3DV: Intelligent 3D Volumetric Video Coding Standard and Platform</span><br>
      <span class="pub-list-authors">
          Jiayu Yang, Luyang Tang, Jiahao Wu, Jie Liang, Feng Gao, Ronggang Wang
      </span>
    </li>
    <li>
      <span class="pub-list-badge">CVPR 2026</span>
      <span class="pub-list-title">Intrinsic Geometry-Appearance Consistency Optimization for Sparse-View Gaussian Splatting</span><br>
      <span class="pub-list-authors">
        Kaiqiang Xiong, Rui Peng, Jiahao Wu, Zhanke Wang, Jie Liang, Xiaoyun Zheng, Feng Gao, Ronggang Wang
      </span>
    </li>
    </li>
      <span class="pub-list-badge">AAAI 2025</span>
      <span class="pub-list-title">Pano-GS: Perception-Aware Gaussian Optimization with Gradient Consistency and Multi-Criteria Densification for High-Quality Rendering</span><br>
      <span class="pub-list-authors">
        Yang Deng, Zhanke Wang, Jiahao Wu, Jie Liang, Jingui Ma, Yang Hu, Ronggang Wang
      </span>
    </li>
    <li>
      <span class="pub-list-badge">Neurips 2025</span>
      <span class="pub-list-title">SAP: Exact Sorting in Splatting via Screen-Aligned Primitives</span><br>
      <span class="pub-list-authors">
        Zhanke Wang, Zhiyan Wang, Kaiqiang Xiong, Jiahao Wu, Yang Deng, Ronggang Wang
      </span>
    </li>
    <li>
      <span class="pub-list-badge">ACMM 2025</span>
      <span class="pub-list-title">Excavating the Most Critical Gaussians: Sparse Selection and Structural Optimization for Efficient 3DGS Compression</span><br>
      <span class="pub-list-authors">
        Yang Hu, Jingui Ma, Yucheng Yang, Jie Liang, Jinbo Yan, Jiahao Wu, Jiayu Yang, Yang Deng, Ronggang Wang
      </span>
    </li>
    <li>
      <span class="pub-list-badge">CVPR 2025</span>
      <span class="pub-list-title">Instant gaussian stream: Fast and generalizable streaming of dynamic scene reconstruction via gaussian splatting</span><br>
      <span class="pub-list-authors">
        Jinbo Yan, Rui Peng, Zhiyan Wang, Luyang Tang, Jiayu Yang, Jie Liang, Jiahao Wu, R Wang
      </span>
    </li>
  </ul>
</div>

<script src="assets/js/show_publications.js"></script>
<script src="assets/js/pub_media_rotator.js"></script>


Services
--------
- Reviewer for CVPR'2026, ICLR'2026, ECCV'2026.

Talks
--------

