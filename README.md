# Fine-tune `distilroberta-base` for token-classification

This repository contains the code to train [distilroberta-base](https://huggingface.co/distilroberta-base) for token-classiciaton using either `conl++`, `wikiANN` or both of them for training. Training can be launched either on a local machine or Amazon SageMaker. 


Features:
- [ ] Earlystopping Callback
- [ ] Load best model at the end
- [ ] Hyperparameter search


## Training

### Launch training

**SageMaker**

You need to define your Hyperparameters, instance_type, instance count in `sagemaker_launcher.py`

```bash
python sagemaker_launcher.py
```

**Local Machine**


```bash
python src/train.py --foo bar
```

### Launch hyperparameter search with ray tune

Inspired/Guided from the [Hugging Face Blog Post "Hyperparameter Search with Transformers and Ray Tune"](https://huggingface.co/blog/ray-tune)

**Local Machine**


```bash
python src/hyperparameter_search_train.py
```

## Results