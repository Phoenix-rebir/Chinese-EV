# **Visual Forecast: Illuminating the Chinese EV Market Growth**
*Project2*
Author: Hongkun Tian, Zhiye Wang, Zilin Wang
Team ID: T9  
Date: 2025-12-17

## **Abstract**

<div style="text-align: justify;">

This project aims to **analyze and improve** a visualization that forecasts the Chinese electric vehicle (EV) market growth, based on data from EV-Volumes. The selected visualization is a complex chart showing China's BEV and PHEV demand, including light vehicle sales, EV volumes, market share, and growth rates. At the beginning of the project, we explained the reasons for the **theme selection** and **reproduce the original chart** using Python. Then, we deeply analyzed the information the visualization tries to convey and **the story it presents**. We also provided ideas for reading it. In addition, we evaluated **the strength and weakness of the original chart**. To address the identified shortcomings, we modified the visualization step by step. In the end, we generated improved visualizations that clearly illustrate the trends in China's EV market, uncovering **new insights** that are difficult to observe in the original visualization.

</div>


<p style="text-align: center;">
    <i>
    <center>
        <img style="border-radius: 0.3125em;width: 80%;" src="https://thk.s3.wangty88.us/ori-china-bev-phev-demand.jpg" alt=""/>
        <br>
        [Figure 1. The original chart]
    </i>
</center>
</p>
<br>

## **Contents**

- [Abstract](#abstract)
- [1. Introduction](#1-introduction)
  - [1.1. Background](#11-background)
  - [1.2. Reasons for Selection](#12-reasons-for-selection)
  - [1.3. Stories in the Chart](#13-stories-in-the-chart)
  - [1.4. The Effectiveness of the Visualization](#14-the-effectiveness-of-the-visualization)
- [2. Problem Statement](#2-problem-statement)
- [3. Modification](#3-modification)
- [4. Conclusion](#4-conclusion)
- [5. Open Source](#5-open-source)
- [6. Acknowledgments](#6-acknowledgments)

## **1. Introduction**

### **1.1. Background**

Imagine a market where electric vehicles (EVs) are not just a trend but a revolution: China's EV boom surged into 2022, skyrocketing market share from 13.9% in 2021 to an astonishing 26.7%. Written by EV-Volumes, this report dives into the heart of China's electrified future, where government targets for new-energy vehicles (NEVs)—encompassing BEVs, PHEVs, and even FCEVs—were smashed three years ahead of schedule. Amid economic headwinds like post-COVID recovery and real-estate woes, forecasts paint a bold picture of unstoppable expansion, promising to reshape transportation and sustainability worldwide.

### **1.2. Reasons for Selection**

We want to study the changes in Chinese EV sales and market penetration. We are interested in the factors affecting EV adoption and future trends in China. This chart comprehensively shows the historical and forecasted EV volumes, market share, and growth rates in China, which attracted our attention. Thus, we select it as our topic.

Generally, we have the following questions:
- What is the **overall trend** of EV sales and market penetration in China?
- How does the EV market share evolve over time in China?
- What are the growth rates and key inflection points in the Chinese market?

To address these questions, we modified the original chart step by step for better visualization and analysis. This visualization highlights trends that could influence global policies on climate change and energy transition, promoting sustainable transportation and reducing carbon emissions.

### **1.3. Stories in the Chart**

We replicated the original chart and translated the Chinese text to English in the legend.

<p style="text-align: center;"><i>
<center>
    <img style="border-radius: 0.3125em;
    box-shadow: 0 2px 4px 0 rgba(34,36,38,.12),0 2px 10px 0 rgba(34,36,38,.08);width: 80%;" 
    src="https://thk.s3.wangty88.us/reproduction.png"alt=""/>
    <br>
  [Figure 2. The reproduced chart]</i></p>
</center>

As shown in figure 2, the chart combines multiple forms of presentation: **bar chart**, **line chart**, and **area fill**.
<br>

- **The bar chart shows the sales volume of BEV and PHEV**, with the left y-axis (in thousands of vehicles).
- **The area fill depicts the light vehicle sales background**.
- **The lines represent the PEV share and growth rate**, aligned with the right y-axis.

We got **the following stories** in the chart:

- EV sales have been increasing rapidly since 2020, with BEV volumes growing faster than PHEV. The market share reached 26.7% in 2022 from 13.9% in 2021, driven by government targets for NEVs (BEVs, PHEVs, FCEVs) being met early.
- The PEV market share has risen from below 1% in 2015 to projected 83% by 2035, with forecasts showing 46% in 2025, 68% in 2030, and 83% in 2035.
- Growth rates peaked around 2021 and are declining as the market matures, but PHEVs have gained share, rising from 18% of EV sales in 2021 to 25% in 2022, largely due to BYD and Li Auto models.
- Despite economic challenges like post-COVID recovery and real-estate issues, the light-vehicle market's resilience supports higher EV volumes, with 2023 forecasts at 33.4% share and 8.35 million units.
- Segment shifts show A-segment EVs declining from 23% in 2021 to 15% in 2022, squeezed by B-segment growth from 1.7% to 5.5%, highlighting consumer preferences for larger models.
<br>

### **1.4. The Effectiveness of the Visualization**
<ul style="line-height: 1.8; margin-top: 10px;">
    <li><strong>Data-Ink Ratio</strong>: <br> The chart contains some redundant elements, such as overlapping bars and lines. From a cognitive perspective, these overlapping elements can overwhelm viewers' working memory, making it harder to process the data efficiently.</li>
    <li><strong>Lie Factor</strong>: <br> The visual changes accurately reflect the data changes.</li>
    <li><strong>Amount of Information</strong>: <br> The chart presents extensive data from 2015 to 2035, delivering valuable insights.</li>
</ul>

---


## **2. Problem Statement**

<ul style="line-height: 1.5; margin-top: 10px;">
    <li style="margin-bottom: 15px;"><strong>The amount of information is too large</strong>, with multiple data series on one chart causing cognitive overload.</li>
    <li style="margin-bottom: 15px;">The <strong>dual y-axes</strong> make it hard to read and compare data.</li>
    <li style="margin-bottom: 15px;">The chart lacks a <strong>clear title</strong> and <strong>axis labels</strong>.</li>
    <li style="margin-bottom: 15px;"><strong>Time-series data should use line charts</strong> for better trend visualization.</li>
    <li style="margin-bottom: 15px;"><strong>Visual variables</strong> could be better used to distinguish data.</li>
    <li style="margin-bottom: 15px;">The x-axis labels are <strong>rotated</strong>, making them hard to read.</li>
    <li style="margin-bottom: 15px;">The bars are too narrow and should be widened.</li>
    <li style="margin-bottom: 15px;">The chart lacks <strong>annotations</strong> to highlight key points.</li>
</ul>

---

## **3. Modification**

**For all modified charts,** we added clear titles, axis labels, and units. We improved readability by separating data into individual charts.

<p style="text-align: center;"><i>
<center>
    <img style="border-radius: 0.3125em; box-shadow: 0 2px 4px 0 rgba(34,36,38,.12),0 2px 4px 0 rgba(34,36,38,.08); width: 80%;" src="https://thk.s3.wangty88.us/modify1.png" alt=""/>
    <br>
    [Figure 3. The modified BEV & PHEV Volume chart]
</i></p>
</center>

**Firstly,** we separated the BEV and PHEV volume data into a line chart with smooth curves and scatter points. We used different colors for BEV and PHEV. We added an annotation for the start of PHEV decline. From this chart, we can clearly see the rapid growth of BEV volumes and the peak and decline of PHEV volumes. BEV volumes have grown exponentially from 0.2 million in 2015 to projected 23.7 million in 2035. PHEV volumes peaked around 2021-2022 and are declining thereafter.

<p style="text-align: center;"><i>
<center>
    <img style="border-radius: 0.3125em; box-shadow: 0 2px 4px 0 rgba(34,36,38,.12),0 2px 4px 0 rgba(34,36,38,.08); width: 80%;" src="https://thk.s3.wangty88.us/modify2.png" alt=""/>
    <br>
    [Figure 4. The modified PEV Share chart]
</i></p>
</center>

**Secondly,** we separated the PEV market share into a dedicated line chart. We highlighted the rapid growth period from 2020 to 2025. This chart focuses on the market penetration trend, showing the accelerating adoption of EVs in China.

<p style="text-align: center;"><i>
<center>
    <img style="border-radius: 0.3125em; box-shadow: 0 2px 4px 0 rgba(34,36,38,.12),0 2px 4px 0 rgba(34,36,38,.08); width: 80%;" src="https://thk.s3.wangty88.us/modify3.png" alt=""/>
    <br>
    [Figure 5. The PEV Growth Rate chart]
</i></p>
</center>

**Thirdly,** we created a chart for PEV growth rates, showing the declining growth as the market matures. Here we observe the growth rate peaking at 120% in 2015 and 2021 and declining to single digits by 2035.


---

## **4. Conclusion**
**In conclusion**, we separated the original complex chart into three focused visualizations: BEV & PHEV Volume, PEV Share, and PEV Growth Rate, revealing clearer trends in China's EV market. Through modification, we uncovered insights about the rapid growth phase, market maturation, and the shift from PHEV to BEV dominance.

Based on these trends, we can promote EV adoption through policy support, infrastructure development, and technology innovation.

This project underscores the importance of excellence in information visualization. By applying principles like the data-ink ratio, which ensures every visual element adds value and avoids redundancy, we reduced cognitive overload in our charts. Cognitive theory reminds us that humans process visuals through preattentive attributes and Gestalt principles, so designs must facilitate quick comprehension. The iterative process of revising and seeking feedback was crucial; without it, our initial cluttered chart would have remained ineffective. Sharing these insights with the community highlights how thoughtful visualization can drive societal change, from informed policy decisions to sustainable practices. We encourage others to prioritize clarity, ethics, and user-centered design in their work.

---

## **5. Open Source**

The open-source code for this project can be found at [https://github.com/Phoenix-rebir/Chinese-EV](https://github.com/Phoenix-rebir/Chinese-EV).

---

## **6. Acknowledgments**

We would like to thank the instructors of the Information Visualization course for their guidance during the work sessions.


<parameter name="filePath">f:\KeCheng\zzl\project2\project2_team9.md
