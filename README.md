# DAML

Source code for the ACL 2019 paper entitled "Domain Adaptive Dialog Generation via Meta Learning" by Kun Qian and Zhou Yu https://arxiv.org/abs/1906.03520


```
@article{qian2019domain,
  title={Domain Adaptive Dialog Generation via Meta Learning},
  author={Qian, Kun and Yu, Zhou},
  journal={arXiv preprint arXiv:1906.03520},
  year={2019}
}
```


## Training with default parameters

```
python model.py -mode train -model [tsdf-camrest|tsdf-kvret]
```

(optional: configuring hyperparameters with cmdline)

```
python model.py -mode train -model [tsdf-camrest|tsdf-kvret] -cfg lr=0.003 batch_size=32
```

## Testing

```
python model.py -mode test -model [tsdf-camrest|tsdf-kvret]
```

## Reinforcement fine-tuning

```
python model.py -mode rl -model [tsdf-camrest|tsdf-kvret] -cfg lr=0.0001
```

## Before running
1. Install required python packages. We used pytorch 0.3.0 and python 3.6 under Linux operating system. 
```
pip install -r requirements.txt
```
2. Make directories under PROJECT_ROOT.
```
mkdir vocab
mkdir log
mkdir results
mkdir models
mkdir sheets
```

3. Download pretrained Glove word vectors and place them in PROJECT_ROOT/data/glove.
