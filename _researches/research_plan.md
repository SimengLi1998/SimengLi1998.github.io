---
layout: page
title: "Research plan 2025"
description:  To develop a recommendation system
img: assets/img/researches/r1_1.png
importance: 1
category: work
related_publications: false
---

## Introduction

The objective of my research is to develop a recommendation system (RS) driven by Large Language Models (LLMs) to provide more personalized and human-centric services across various downstream applications such as music recommendation, product recommendation, app recommendation, and movie recommendation. Conventional Recommendation Models (CRMs) face significant limitations, including a lack of open-domain world knowledge and insufficient explainability of recommendations.
The emergence of large foundation models, particularly LLMs, offers promising and universal insights for addressing challenging problems in the data mining field. These models demonstrate impressive general intelligence across various language processing tasks due to their extensive memory of open-world knowledge, logical and commonsense reasoning capabilities, and awareness of human society and culture. By leveraging natural language as a universal information carrier, LLMs can integrate, exploit, and interpret knowledge across different forms, modalities, domains, and platforms.[1]
My research interest aims to explore the incorporation of LLMs into recommender systems to overcome the inherent drawbacks of CRMs by utilizing LLMs' common knowledge and reasoning abilities. The goal is to enhance the performance and user experience of recommendation systems, making them more intelligent, explainable, and effective in understanding and catering to user needs across various application domains.

## Literature Review

Recently, RS researchers and practitioners have made pioneering attempts to employ Large Language Models (LLMs) in current recommendation pipelines, achieving notable progress in enhancing the performance of various canonical recommendation processes such as feature modeling and ranking. Several survey works delve into the potential of LLMs for general recommender systems:

 - Wu et al. [2] conduct a review on both discriminative and generative LLMs for recommendation with different tuning strategies.

 - Fan et al. [3] focus on the pretraining, finetuning and prompting approaches when leveraging LLM for recommendation.

 - Huang et al. [4] investigate the recommendation foundation models from aspects of both different model types and various downstream tasks.

According to the research of previous scholars and the current state-of-the-art [1,5], there are three primary approaches for LLM-driven recommendation systems:

1.	Sequential Integration of LLM and RS (Serial Approach)

2.	LLM as a Replacement for Traditional RS Architecture (LLM as RS)

3.	Fusion of LLM and RS (Fusion Approach)

![](/assets/img/researches/r1_1.png)



### Approach 1: Sequential Integration of LLM and RS

This approach involves using LLMs to process upstream data before inputting it into the recommendation system for final ranking and decision-making. There are two main paradigms:

- LLM Embeddings + RS: LLM generates embeddings for items and users, which are then input into the recommendation system. E.g., Xiaohongshu's "NoteLLM: A Retrievable Large Language Model for Note Recommendation" [6]

- LLM Tokens + RS: LLM processes raw text data from users and items directly and then passes the processed results to the recommendation system. E.g., Huawei's "CTRL: Connect Collaborative and Language Model for CTR Prediction" [7]



### Approach 2: LLM as RS

In this approach, LLMs are used directly as recommendation systems. This method leverages the generative capabilities of LLMs by constructing detailed prompts and instructions, enabling the LLM to generate recommendations based on user and item information. E.g., Meta's "Actions Speak Louder than Words: Trillion-Parameter Sequential Transducers for Generative Recommendations" [8]

![](/assets/img/researches/r1_2.png)
![](/assets/img/researches/r1_3.png)


### Approach 3: Fusion of LLM and RS

This approach addresses both the "WHERE" and "HOW" questions of integrating LLMs into RS:

 - WHERE: Discusses the roles that LLMs could play at different stages of the recommendation system pipeline, from data collection to the recommendation pipeline controller. The modern deep learning-based recommender systems can be characterized as an information cycle encompassing six key stages:

      1.	Data Collection: Gathering user feedback data.

      2.	Feature Engineering: Preparing and processing the collected raw data.

      3.	Feature Encoder: Transforming data features into neural embeddings.

      4.	Scoring/Ranking Function: Selecting and ordering the recommended items.

      5.	User Interaction: Determining how users engage with the recommendations.

      6.	Recommendation Pipeline Controller: Serving as the central mechanism tying all the stages together in a cohesive process.

 - HOW: Centers on how to adapt LLMs for RS, with two orthogonal taxonomy criteria:

      1.	Parameter Freezing: Whether to freeze the parameters of the LLM during the training phase.

      2.	Involvement of CRM: Whether to involve conventional recommendation models (CRM) during the inference phase.





**Research Plan**

![](/assets/img/researches/r1_4.png)

1.	Comparison of LLM+RS Research Paradigms
       - Conduct a comparative analysis of the three mainstream LLM+RS research approaches: sequential integration, LLM as RS, and fusion of LLM and RS.
       - Perform experimental comparisons to evaluate the strengths and limitations of each approach.
       - Establish effective evaluation criteria to assess the performance and suitability of these approaches.
2.	Exploring Solutions to Current RS Drawbacks with LLM Integration
      Investigate whether the integration of LLMs can address the current limitations of recommendation systems, such as:
       - How can LLMs help solve the cold start problem and improve recommendation performance for new users or new content?
       - Can LLMs help mitigate the information cocoons effect and expand user interests?
       - How can LLMs facilitate the effective recommendation of non-popular, long-tail content?
       - In what ways can LLMs enhance the understanding of complex user intentions and contexts?
       - How can LLM-driven recommendation systems provide more explainable recommendations to users?
3.	Downstream Applications of LLM+RS Systems
       - Explore how LLM+RS systems can influence product diversity sales and the long-tail effect.
       - Investigate the potential of LLM+RS systems to facilitate cross-business and cross-company recommendations.
       - Study how LLM+RS systems can integrate data from different business lines to provide a more comprehensive user profile.
       - Utilize LLMs to deeply understand user behavior and decision-making processes in recommendation systems.
       - Ensure that LLM-driven recommendation systems adhere to ethical standards and promote fairness:
      	How can LLM+RS systems balance personalization and social diversity in recommendations?
      	Can LLMs help reduce biases related to gender, race, and other factors in recommendation systems?
       - Explore the feasibility of LLM+RS systems for recommendations across platforms, regions, fields, and languages.

[1] https://arxiv.org/pdf/2306.05817

[2] Likang Wu, Zhi Zheng, Zhaopeng Qiu, Hao Wang, Hongchao Gu, Tingjia Shen, Chuan Qin, Chen Zhu, Hengshu Zhu, Qi Liu, et al. 2023. A Survey on Large Language Models for Recommendation. arXiv preprint arXiv:2305.19860 (2023).

[3] Wenqi Fan, Zihuai Zhao, Jiatong Li, Yunqing Liu, Xiaowei Mei, Yiqi Wang, Zhen Wen, Fei Wang, Xiangyu Zhao, Jiliang Tang, and Qing Li. 2023. Recommender Systems in the Era of Large Language Models (LLMs). arXiv:2307.02046 [cs.IR]

[4] Chengkai Huang, Tong Yu, Kaige Xie, Shuai Zhang, Lina Yao, and Julian McAuley. 2024. Foundation Models for Recommender Systems: A Survey and New Perspectives. arXiv preprint arXiv:2402.11143 (2024).

[5] https://arxiv.org/pdf/2305.19860

[6] https://arxiv.org/pdf/2403.01744

[7] https://arxiv.org/pdf/2306.02841   

[8] https://arxiv.org/abs/2402.17152 
