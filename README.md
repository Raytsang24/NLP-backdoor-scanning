# Discovery of Unsafe Models Shared on Hugging Face Platform

We are conducting a research on the detection of NLP backdoor models. We have utilized our algorithm to scan Transformer-based NLP models on Hugging Face and surprisingly found one of them with a high probabilitiy of containing a ***hidden backdoor***:

- https://huggingface.co/JungleLee/bert-toxic-comment-classification (190,000+ downloads last month, timestamp: 2024/4/14)

We provide some test samples (in .csv files) that could trigger backdoor-like behaviors of the model but are correctly classified by benign models. Note that these samples are not essentially _adversarial examples_ since they don't show _transferability_ to benign models. Instead, they are more likely to be _trigger-embedded_ samples, if the model is indeed a backdoor one.

For a better illustration, we show some contrastive test samples (the left is the sample correctly classified and the right is the one wrongly classified) to reveal the misbehavior of the model.

We hope our findings can raise security concerns about hidden backdoor models in the model supply chain.

<p align = "center">    
<img  src="demo_example/clean_1.JPG" width="500" />
<img  src="demo_example/poison_1.JPG" width="500" />
</p>

<p align = "center">    
<img  src="demo_example/clean_2.JPG" width="500" />
<img  src="demo_example/poison_2.JPG" width="500" />
</p> 

<p align = "center">    
<img  src="demo_example/clean_3.JPG" width="500" />
<img  src="demo_example/poison_3.JPG" width="500" />
</p> 


