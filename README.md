# Image Captioning Systsme
This repository presents a pyTorch implementation of the Attend, Show, and Tell paper \url{https://arxiv.org/pdf/1502.03044.pdf}  and applies two extentions to it. The first is a method to utalize the GloVe embeddings and the second is a method that integrates BERT into training. These extensions have proved to greatly inhance the models performance.

Parts of this pyTorch implementaion is taken from the following github repositories:
1. https://github.com/parksunwoo/show_attend_and_tell_pytorch/blob/master/prepro.py
2. https://github.com/sgrvinod/a-PyTorch-Tutorial-to-Image-Captioning

The main additions of this implementaion are:
1. Integrating GloVe
2. Intergrating BERT
3. Integrating recent advancements into the model implementation
3. Simplifying and cleaning the older implementations

# Instructions to run the code

1. Create three folders: (1) data, (2), data>annotations, and (3) glove.6B
1. Download the train2014 and val2014 COCO dataset and place it in the data folder
2. Download the COCO train/val 2014 captions and place them in data>annotations
3. Run the processData.py file (uncomment the last time of that file first) - this will generate train2014_resized, val2014_resized, vocab.pkl

4. Download the glove.6B dataset and place it in glove.6B
5. Run the glove_embeds.py file - this will generate glove_words.pkl in the glove.6B folder

6. Open main.py and scroll to 'START Parameters' (Pre-Trained Models: Baseline, GloVe, BERT)
7. Edit the parameters to train/test the particular model you want 
8. Run main.py with python3


# Pre-Trained Models
1. BERT Soft Attention Model
2. GloVe Soft Attention Model
3. Baseline Soft Attention Model

# Pre-Trained Models

If you only want to validate Pre-Trained Models, then it's much simpler to use the Jupyter Notebook in this repository and just load the model you wish to validate. Open the notebook and find the Load model section and pick the model you want. If you would like to compare all the models against each other, open the jupeter notebook and run it without changing any of the code.