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
   
   [code commit week 2](https://github.com/HishamJuneidi/Capston-ll/commit/aab642318f31b46708fe0809b93ae6d31c7ea010)
 
- **Week 3 :** Working on the Tiger audio calssification Moan/No Moan sound
    1. Preprocess the data and prepare the audio clip by cutting the clip to 3 sec time length
    2. Remove any noise data and convert the 3 sec clip 16HZ then to images as bellow :
    
   ![SMM01167_20221109_182902_77_reduced](https://user-images.githubusercontent.com/33138418/218593596-145fa3a7-b0df-40a9-9292-d2dad27c3e38.png)
   
   3. Convert each imges to spectorm as bellow :

    ![Screen Shot 2023-02-13 at 5 54 22 PM](https://user-images.githubusercontent.com/33138418/218594086-dfe0dfe8-4657-47ff-a8c4-c504d360567a.png)
    
  [code commit week 3](https://github.com/HishamJuneidi/Capston-ll/commit/fdad1c7b41b0ba2c14dea722fedad71552e882d8)
  
- **Week 4 :** Extend the work that had been done on Tiger calls classifications to use it for Leopard Saws classifications. First step was to check small sample of of Saws vs. No Saw calls and then build 100 dataset for each class (totale 200 samples).

- **Week 5 :** Training the dataset on the generated images for Saws and No Saws for 30 epoch. The images below is a sample. The blue represent a Saw and brown represent No Saw.
 
    ![Screen Shot 2023-03-07 at 1 38 21 PM](https://user-images.githubusercontent.com/33138418/223519187-ae9ffb52-aa53-4762-b134-e84847f97926.png)
    
    [code commite week 5](https://github.com/HishamJuneidi/Capston-ll/commit/59a72be8f68e4a5926f323b433b84d420825c214)

- **Week 7 :** Worded on clearing the code and making the code handle multiple audio clips at once. I created a time formate to idantify where in the audio clip did the leopard saw happen. 




