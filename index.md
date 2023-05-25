---
layout: default
title: "Home"
toc: true
url: /
---
#### **Welcome to SSS&SDS Group!**
SSS&SDS group belongs to [Data Storage and Application Lab](http://storage.hust.edu.cn/). SSS means Solid State Storage, while SDS indicates Software Defined Storage. We aim at building high performance and energy-efficient systems with emerging devices and technologies (e.g., non-volatile memories, key-value storage, solid-state drive, high performance compression, cloud object store).

Our group has published several papers on international conferences like ISCA, DAC, DATE, ICCAD, ICPP, MSST, ICCD, LCTES, etc. as well as some top journals including IEEE TC, IEEE TCAD, IEEE T-ED, ACM TACO, ACM TODAES, JSA, etc.


<head>
    <meta charset="utf-8">
    <title>picplay</title>
    <style>
        #divout {
            max-width: 600px;
            max-height: 400px;
            position: relative;
            margin: 0 auto;
        }

        .imgdiv img {
            width: 100%;
        }
    
        .imgdiv {
            display: none;
        }
    
        .dotdiv {
            text-align: center;
            position: absolute;
            width: 100%;
            bottom: -30px;
        }
    
        .dot {
            width: 16px;
            height: 16px;
            display: inline-block;
            background: #bbbbbb;
            border-radius: 10px;
            margin: 0 12px;
        }
    
        .title {
            font-size: 18px;
            color: #0099FF;
            position: absolute;
            text-align: center;
            font-weight: 700;
            width: 100%;
            bottom: 10px;
        }
    
        .active {
            background-color: #717171;
        }
    
        #arrow {
            position: absolute;
            top: 50%;
            margin-top: -30px;
            width: 100%;
            opacity: .3;
            transition: opacity 2s;
        }
    
        #divout:hover #arrow {
            opacity: .9;
        }
    
        #arrow img {
            cursor: pointer;
        }
    
        .imgdiv {
            animation: fade 1.5s;
        }
    
        @keyframes fade {
            from {
                opacity: .3;
            }
    
            to {
                opacity: 1;
            }
        }
    </style>
</head>

<body>
    <!--    div#divout>(div.imgdiv>img+div.title{标题文本$})*4 +(div.dotdiv>span.dot*4)-->

    <div id="divout">
        <div class="imgdiv" style="display: block">
            <img src="/assets/img/league_building/2021_11_autumn.png" height="80%" width="80%" alt="">
            <div class="title">Group Party 2021</div>
        </div>
        <div class="imgdiv">
            <img src="/assets/img/league_building/2020_group_party.jpg" height="80%" width="80%" alt="">
            <div class="title">Group Party 2020</div>
        </div>
        <div class="imgdiv">
            <img src="/assets/img/award.png" height="80%" width="80%" alt="">
            <div class="title">OlympusMons Award</div>
        </div>
        <div class="imgdiv">
            <img src="/assets/img/ICCD19.jpg" height="80%" width="80%" alt="">
            <div class="title">ICCD 2019</div>
        </div>
        <div class="imgdiv">
            <img src="/assets/img/ICCD17.jpg" height="80%" width="80%" alt="">
            <div class="title">ICCD 2017</div>
        </div>
        <div class="imgdiv">
            <img src="/assets/img/DATE19.jpg" height="80%" width="80%" alt="">
            <div class="title">DATE 2019</div>
        </div>
        <div class="imgdiv">
            <img src="/assets/img/2021.jpg" height="80%" width="80%" alt="">
            <div class="title">Graduates in 2021</div>
        </div>
        <div class="dotdiv">
            <span class="dot active"></span>
            <span class="dot"></span>
            <span class="dot"></span>
            <span class="dot"></span>
            <span class="dot"></span>
            <span class="dot"></span>
            <span class="dot"></span>
        </div>
        <div id="arrow">
            <img src="/assets/img/left.png" alt="" width="60" onClick="picplay(false)">
            <img src="/assets/img/right.png" width="60" alt="" align="right" onClick="picplay(true)">
        </div>
    </div>

</body>

<script>
    var imgIndex = 0;
    var imgDivArr = document.getElementsByClassName("imgdiv");
    var dotArr = document.getElementsByClassName("dot");
    /**
     *  播放图片
     *  参数r：是否正放，若为true，正放。若为false，倒放
     */
    function picplay(r) {
        for (let i = 0; i < imgDivArr.length; i++) {
            imgDivArr[i].style.display = "none";
            dotArr[i].className = "dot";
        }
        if (r) {
            imgIndex++;
            imgIndex = (imgIndex >= imgDivArr.length) ? 0 : imgIndex;
        } else {
            imgIndex--;
            imgIndex = (imgIndex < 0) ? imgDivArr.length - 1 : imgIndex;
        }
        imgDivArr[imgIndex].style.display = "block";
        dotArr[imgIndex].className = "dot active";
    }
    setInterval(picplay, 6000, true);

</script>





#### **News**
- Our paper "ODLPIM: A Write-Optimized and Long-Lifetime ReRAM-based accelerator for online deep learning" is accepted by [DATE 2023](https://www.date-conference.com/date-2023-accepted-papers). Congratulations to [Heng Zhou]
- Our paper "ZNSKV: Reducing Data Migration in LSMT-Based KV Stores on ZNS SSDs" is accepted by ICCD, 2022. Congratulations to Denghui Wu.
- Our paper "RMMIO: Enabling Reliable Memory-Mapped I/O for Persistent Memory Systems" is accepted by ICCD, 2022. Congratulations to Bo Ding.
- Our paper "MORE<sup>2</sup>: Morphable Encryption and Encoding for Secure NVM" is accepted by [ICCAD 2021](https://iccad.com/index.php). Congratulations to [Wei Zhao](https://thiszw.top).  
- Our paper "CERES: Container-Based Elastic Resource Management System for Mixed Workloads is accepted by [ICPP 2021](https://oaciss.uoregon.edu/icpp21/). Congratulations to [Jinyu Yu](https://yujinyu.site). 
- Our paper "Better atomic writes by exposing the flash out-of-band area to file systems" is accepted by [LCTES 2021](https://pldi21.sigplan.org/home/LCTES-2021#event-overview). Congratulations to Hongwei Qin.  
- Our paper "Improving the energy efficency of STT-MRAM based approximate cache" is accepted by [DATE 2021](https://www.date-conference.com/). Congratulations to [Wei Zhao](https://thiszw.top).  
- Our paper "MorLog: Morphable Hardware Logging for Atomic Persistence in Non-Volatile Main Memory" is accepted by [ISCA 2020](https://iscaconf.org/isca2020/). Congratulations to Xueliang Wei.  

**We are looking for motivated undergraduates and master students to join the team, please feel free to contact me. (Email: tongwei@hust.edu.cn)**