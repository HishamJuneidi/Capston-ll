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




