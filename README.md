<!-- 
  <<< Author notes: Header of the course >>> 
  Include a 1280×640 image, course title in sentence case, and a concise description in emphasis.
  In your repository settings: enable template repository, add your 1280×640 social image, auto delete head branches.
  Add your open source license, GitHub uses Creative Commons Attribution 4.0 International.
-->
# Hisham Juneidi

# Animal Calls detection Using Neural Network 

## Motivation

Studying Leopard vocalizations requires spending hundreds of hours to Listen and annotate audio calls. We created an automated vocalization detector that can extract animal calls from recordings obtained by a song meter audio recorder placed at the Connecticut Beardsley zoo’s leopard enclosure.



## Installation

```
pip install h5py
pip install typing-extensions
pip install wheel

pip install noisereduce
pip install pydub
pip uninstall tensorflow
pip uninstall tensorflow-gpu
pip uninstall tensorflow-io
pip install tensorflow 
pip install --no-deps tensorflow-io
```
## Expectation

Once the CNN is trained, the script creates two types of CSV files. First type to identify the Leopards' Saws in each interval for each audio clip. Second type is to identify the number of saws for each audio clip.

## Collaborative

Hisham Juneidi (CS), Hammad Mansoor(CS), Likitha Varapana(CS)
Dr. Danushka Bandara (CS), Dr. Ashley Byun (Biology)


## Capston ll Weekly Updates Timeline:

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

- **Week 7 :** Worded on clearing the code and making the code handle multiple audio clips at once. I created a time formate to idantify where in the audio clip did the leopard saw happen as shown below:

    SMM07257_20221118_003302_16BIT.wav

    Index 164 | Audio Clip Time Interval 0:08:12 \
    Index 165 | Audio Clip Time Interval 0:08:15 \
    Index 234 | Audio Clip Time Interval 0:11:42 \
    Index 237 | Audio Clip Time Interval 0:11:51 

    [code commite week 7](https://github.com/HishamJuneidi/Capston-ll/commit/1ca320bbdb7f4ebc9b44380c854f316fffe5fde7#diff-af60dcd73c8e9eab485922c6e17622fe554e7cbdbfa254c08be298709704bc93)
    
- **week 8 :** This week was about implementing Saliency map to understand what the CNN see when it evaluate/classify the model. 
Saliency maps is a technique to rank the pixels in an image based on their contribution to the final score from a Convolution Neural Network. The technique is described in great detail in this [paper](https://arxiv.org/pdf/1312.6034v2.pdf)

  The figure below shows the borders were the CNN build to classify a Leopard Saw based on each pixel:

![Screen Shot 2023-03-30 at 3 37 25 PM](https://user-images.githubusercontent.com/33138418/229618779-d9ae1327-0607-4ae4-b645-bafabae29fbc.png)

   The figure belwo shows the CNN looking to a non Leopard Saw :

![Screen Shot 2023-04-03 at 4 31 54 PM](https://user-images.githubusercontent.com/33138418/229621114-f7e3ff5b-cacd-4f5e-9f38-d477bf2fe8b4.png) 

   [code commite week 8](https://github.com/HishamJuneidi/Capston-ll/commit/63cb7a2fd03aae870af82cdf65b274d29b23776b)
    
- **week 9 :** We found using CNN by itself is not enough and we get many classification like metal banging sound to be classified as Leopard Saw. We used a combination of CNN and Fast Fourier Transform (FFT) methods and with a threshold between 0.4 and 0.1 for FFT to give ous a much higher accuracy. The figure below shows the FFT for Saw and none Saw:

![Screen Shot 2023-04-30 at 7 12 26 PM](https://user-images.githubusercontent.com/33138418/235380523-2081d35c-47c0-4afa-a04f-6bbbd056b7da.png)

The table below is used to compare the best method to use for the Hight accuracy results. Our goal is the predicate when we have a Leopard call. The red columns show where is an actual call and the green shows why the combinations of CNN and FFT end up with the most accuracy way for predication. Each time interval is three-second time frame. The time frame that is not mentioned in the figure blow did not have and predication from any mothed. So, to save room, we did not include it. This data is from SMM07257_20221118_033302.wav (one hour audio clip). The annotation is coming from specialized biologist team that work classily with Leopard and to understand their behaviors. We also have Metal Banging class that shows where are the actual Metal banging noises happen and to make it easy to compare each model with what seems a False Positive data (FP).

![Screen Shot 2023-04-30 at 7 21 14 PM](https://user-images.githubusercontent.com/33138418/235380624-5bee2233-542c-48ce-8500-cf1c87211a55.png)

[code commite week 9](https://github.com/HishamJuneidi/Capston-ll/commits/main/AudioClassifier_CNN_and_FFT.ipynb)








