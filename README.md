<!-- 
  <<< Author notes: Header of the course >>> 
  Include a 1280×640 image, course title in sentence case, and a concise description in emphasis.
  In your repository settings: enable template repository, add your 1280×640 social image, auto delete head branches.
  Add your open source license, GitHub uses Creative Commons Attribution 4.0 International.
-->
# Hisham Juneidi


## Capston ll Weekly Updates:

- **Week 1 :** Syllabus week. Create Github and Blog page.
- **Week 2 :** Read about publications that are realted to the missing text problem. Bellow is a summary about each paper I read: <br />  
 A) [RoBERTa](https://arxiv.org/pdf/1907.11692.pdf). July 26, 2019 : 
  refers to a new receipt for training BERT to achieve better results, as they found that the original BERT model is significantly undertrained. The receipt contains the following learnings:
  1.	Train for longer with bigger batch size.
  2.	Remove the next sentence prediction (NSP) task.
  3.	Use longer sequences in training data format. The paper found that using individual sentences as inputs hurts downstream performance. Instead we should use multiple sentences sampled contiguously to form longer segments.
  4.	Change the masking pattern dynamically. The original BERT applies masking once during the data preprocessing stage, resulting in a static mask across training epochs. RoBERTa applies masks in 10 different ways across 40 epochs.

  B) [Should You Mask 15% in Masked Language Modeling? ](https://arxiv.org/pdf/2202.08005.pdf) May 22, 2022 :
  Finding that 30 – 40 of [MASK]ing dataset can improve results of filling the blank/missing tokens.
 
  ![image](https://user-images.githubusercontent.com/33138418/217118821-d4385fac-2757-4710-8c6e-88fbde07e904.png)
  
  C) [BART](https://arxiv.org/pdf/1910.13461.pdf) Oct. 29, 2019 : 
  It combines Bidirectional and AutoRegressive Transformer: 
  
  ![image](https://user-images.githubusercontent.com/33138418/217119484-0730befc-a65d-4768-b397-eda7164235ca.png)

   **SUMMERY : RoBERTa is the most relevant to our goal/ filling missing text**
   [code commit](https://github.com/HishamJuneidi/Capston-ll/commit/aab642318f31b46708fe0809b93ae6d31c7ea010)
 
- **Week 3 :** Working on the Tiger audio calssification Moan/No Moan sound
    1. Preprocess the data and prepare the audio clip by cutting the clip to 3 sec time length
    2. Remove any noise data and convert the 3 sec clip to images as bellow:
    
   ![SMM01167_20221109_182902_77_reduced](https://user-images.githubusercontent.com/33138418/218593596-145fa3a7-b0df-40a9-9292-d2dad27c3e38.png)


    





