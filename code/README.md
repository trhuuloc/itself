# ITSELF: Attention Guided Fine-Grained Alignment for Vision–Language Retrieval (WACV 2026)

---

## 🌟 Highlights
- We propose ITSELF framework. A novel attention-guided implicit local alignment framework, ITSELF with GRAB that leverages encoder attention to mine fine-grained discriminativecues and reinforce global text-image alignment without additional supervision.
- Robust Selection & Scheduling. We propose MARS, which fuses attention across layers and performs diversity-aware top-k selection; and ATS, which anneals the retention budget from coarse to fine over training to stabilize learning and prevent early information loss.

![ITSELF Framework](image/ITSELF.png)


## 🚀 Getting Started
### 1. Requirements
```
docker run --gpus all -it --rm -v $(pwd):/workspace --shm-size=8g itself
```
or
```
pytorch >= 1.9.0
torchvision >= 0.10.0
prettytable
easydict
```


### 2. Prepare Datasets

Download the CUHK-PEDES dataset from [here](https://github.com/ShuangLI59/Person-Search-with-Natural-Language-Description), ICFG-PEDES dataset from [here](https://github.com/ShuangLI59/Person-Search-with-Natural-Language-Description), and RSTPReid dataset from [here](https://github.com/NjtechCVLab/RSTPReid-Dataset).

Organize them in 'data' folder as follows:

```
|-- data/
|   |-- <CUHK-PEDES>/
|       |-- imgs
|            |-- cam_a
|            |-- cam_b
|            |-- ...
|       |-- reid_raw.json
|
|   |-- <ICFG-PEDES>/
|       |-- imgs
|            |-- test
|            |-- train
|       |-- ICFG_PEDES.json
|
|   |-- <RSTPReid>/
|       |-- imgs
|       |-- data_captions.json
```

## 🏋️ Training
```bash
bash run.sh
```

## 🧪 Testing
```bash
python3 test.py
```

## 🙏 Acknowledgments

Some components of this code implementation are adopted from [IRRA](https://github.com/anosorae/IRRA), [RDE](https://github.com/QinYang79/RDE). We sincerely appreciate their contributions.




