# SSLLAP
This repository contains the code for 
Self-Supervised Learning with Attention-based Latent Signal Augmentation for Sleep Staging with Limited Labeled Data

If the code or the paper has been useful in your research, please add a citation to our work: 

# Dependencies
- Python3
- CPU or NVIDIA GPU

# Datasets 
For our paper, you can train on SleepEDFX or ISRUC by downloading data from here. 
We put test data of SleepEDFX on data folder. 

# Training
In order to train a model for SSLLAP, use the main.py script. 
Following are the main parameters for training:
<pre><code>
--klwt : importance of pair wise representation loss 
--segment : number of segment you want to use
--lambda_g : importance of global loss
--lambda_l : importance of local loss
</code></pre>

As an example, in order to train our model, use the following: 
<pre><code>
python main.py --klwt 10 --segment 6 --lambda_g 0.5 --lambda_l 0.5
</code></pre>

# Evaluation
After learning representation, use finetune.py to evaluate model.
<pre><code>
python finetune.py
</code></pre>
