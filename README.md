<div align="center">

# MapGlue: Multimodal Remote Sensing Image Matching

</div>

<div align="center">

Peihao Wu, Yongxiang Yao*, Wenfei Zhang, Dong Wei, Yi Wan, Yansheng Li, Yongjun Zhang*<br>
School of Remote Sensing Information Engineering, Wuhan University<br>
(*)Corresponding author.

## [Paper (arXiv)](https://arxiv.org/abs/2503.16185)

</div>


## Abstract
Multimodal remote sensing image (MRSI) matching is pivotal for cross-modal fusion, localization, and object detection, but it faces severe challenges due to geometric, radiometric, and viewpoint discrepancies across imaging modalities. Existing unimodal datasets lack scale and diversity, limiting deep learning solutions. This paper proposes MapGlue, a universal MRSI matching framework, and MapData, a large-scale multimodal dataset addressing these gaps. Our contributions are twofold. MapData, a globally diverse dataset spanning 233 sampling points, offers original images (7,000×5,000 to 20,000×15,000 pixels). After rigorous cleaning, it provides 121,781 aligned electronic map–visible image pairs (512×512 pixels) with hybrid manual-automated ground truth, addressing the scarcity of scalable multimodal benchmarks. MapGlue integrates semantic context with a dual graph-guided mechanism to extract cross-modal invariant features. This structure enables global-to-local interaction, enhancing descriptor robustness against modality-specific distortions. Extensive evaluations on MapData and five public datasets demonstrate MapGlue’s superiority in matching accuracy under complex conditions, outperforming state-of-the-art methods. Notably, MapGlue generalizes effectively to unseen modalities without retraining, highlighting its adaptability. This work addresses longstanding challenges in MRSI matching by combining scalable dataset construction with a robust, semantics-driven framework. Furthermore, MapGlue shows strong generalization capabilities on other modality matching tasks for which it was not specifically trained.

<img width="4811" height="1348" alt="multi_matching_5_0319_github" src="https://github.com/user-attachments/assets/fc9d7ce7-7363-4f8e-ac5a-2a4f9080daeb" />
Fig. 1. Qualitative Results of Multimodal Image Matching. "``Easy``," "``Normal``," and "``Hard``" denote different levels of transformations applied to the images.

## MapData Dataset
<img width="2652" height="1617" alt="数据集分布_2_github" src="https://github.com/user-attachments/assets/bca52e77-838d-4876-9f45-36b65a8fce94" />
Fig. 2. Geographic Distribution of Sampled Images in the MapData Dataset.

MapData is a globally diverse dataset spanning ``233`` geographic sampling points. It offers original high-resolution images ranging from 7,000×5,000 to 20,000×15,000 pixels. After rigorous cleaning, the dataset provides ``121,781`` aligned electronic map–visible image pairs (each standardized to 512×512 pixels) with hybrid manual-automated ground truth—addressing the scarcity of scalable multimodal benchmarks.

Within the MapData structure, each of the 233 folders represents a unique geographic sampling point. Inside each folder, there are three subfolders (named ``1``, ``2``, and ``3``) corresponding to three different image pairs sampled at that location. Each subfolder further contains two directories: ``L`` for source images and ``R`` for target images.  
### Data format  
```text
MapData/
├── 001/             # sampling points
│   ├── 1/
│   │   ├── L/       # Source images
│   │   └── R/       # Target images
│   ├── 2/
│   │   ├── L/
│   │   └── R/
│   └── 3/
│       ├── L/
│       └── R/
└── ...
```

The ``MapData-test`` dataset can be obtained at following links:<br>
(1) google drive https://drive.google.com/file/d/1VQSyIzs_0X15OH1aXVxeSii0JZmW9WzL/view?usp=sharing<br>
(2) baidu drive https://pan.baidu.com/s/1zMR6V4zNPK8azU5w9rrUuQ  Extract code: ``2ym1``. <br>

### Demo
🚀 **[Try MapGlue Online](https://huggingface.co/spaces/wupeihao/MapGlue)** - Interactive demo on Hugging Face Spaces

# Citation
If you find our work useful in your research, please consider giving a star ⭐ and a citation
```python
@article{wu2025mapglue,
  title={MapGlue: Multimodal Remote Sensing Image Matching},
  author={Wu, Peihao and Yao, Yongxiang and Zhang, Wenfei and Wei, Dong and Wan, Yi and Li, Yansheng and Zhang, Yongjun},
  journal={arXiv preprint arXiv:2503.16185},
  year={2025}
}
```




