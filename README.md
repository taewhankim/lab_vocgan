# Modifed Codes
## Environment
```
pytorch = 1.7
python = 3.7.6
```

## Process

### 1. Make Mel_file with wav files

```
pip install -r requirements.txt

* If you use data other than "kss dataset", change audio parameter in "nvidia_prepro_default.yaml"

  python nvidia_preprocessing.py --data_path /mnt/research/datasets/speech/kss --config config/nvidia_prepro_default.yaml

```

### 2. Train Vocoder with mel file



```
1. setting configs
 
  * split your audio data with train/val
  * set your_audio_data_path & mel_data_path
  * If you use data other than "kss dataset", change audio parameter.

    cd config/configs.yaml

2. train

  python trainer.py -c [config yaml file] -n [name of the run]
  
  python trainer.py -c config/configs.yaml -n kss_vocgan4

```
---

