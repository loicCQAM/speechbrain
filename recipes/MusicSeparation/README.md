# Speech separation with WSJ0MIX
This folder contains a recipe for music separation that supports training with [ConvTasnet](https://arxiv.org/abs/1809.07454)

Additional dependency:
```
pip install mir_eval
```

To run it:

```
python train.py hyperparams/convtasnet.yaml
```
Note that during training we print the negative SI-SNR (as we treat this value as the loss).


# Dataset creation
* The training dataset is created using RAW audio files
* The testing dataset is imported from the musdb library


# Results

Here are the SDR results on the test set.

| | SDR |
|--- | --- |
|Mean | 1.42 |
|Median | 2.29 |


# Training Time
Each epoch takes about 2-3 hours on Google Colab Pro.

# **About SpeechBrain**
- Website: https://speechbrain.github.io/
- Code: https://github.com/speechbrain/speechbrain/
- HuggingFace: https://huggingface.co/speechbrain/


# **Citing SpeechBrain**
Please, cite SpeechBrain if you use it for your research or business.

```bibtex
@misc{speechbrain,
  title={{SpeechBrain}: A General-Purpose Speech Toolkit},
  author={Mirco Ravanelli and Titouan Parcollet and Peter Plantinga and Aku Rouhe and Samuele Cornell and Loren Lugosch and Cem Subakan and Nauman Dawalatabad and Abdelwahab Heba and Jianyuan Zhong and Ju-Chieh Chou and Sung-Lin Yeh and Szu-Wei Fu and Chien-Feng Liao and Elena Rastorgueva and François Grondin and William Aris and Hwidong Na and Yan Gao and Renato De Mori and Yoshua Bengio},
  year={2021},
  eprint={2106.04624},
  archivePrefix={arXiv},
  primaryClass={eess.AS},
  note={arXiv:2106.04624}
}
```
