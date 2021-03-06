# GANSage

## Baselines
- NileTMRG (SemEval-2017 Task 8)
- LSTM + GraphSage
- Tweet2vec + GraphSage 
- VAE + GraphSage

## Methodology
- We extract two different embeddings to represent the text and the graph structure seperately.
- GAN is trained on the text so that the embeddings in GAN can be used as one task of the multi-task model.
- GAN learning is halted when the discriminator guesses the results from the generator.
- GraphSAGE model is used to learn the graph structure and those embeddings are used for the representation of the structure.
- Finally these two embeddings are sent to a multi-task model which will run on a classification task of rumour/not-rumour.

## Metrics
- Macro F1
- Accuracy

## Dataset
- PHEME: https://figshare.com/articles/PHEME_dataset_for_Rumour_Detection_and_Veracity_Classification/6392078

## Results
- NileTMRG: 0.56, 0.56
- VAE + GraphSage: 0.62, 0.62
- Tweet2vec + GraphSage: 0.64, 0.64
