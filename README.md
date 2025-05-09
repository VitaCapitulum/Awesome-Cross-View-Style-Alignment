# Awesome Domain Style Alignment

* 8bit 흑백 항공정사영상과 11bit 초소형 전정색 영상 간의 도메인 차이와 미세 기하학적 오차를 보정
    * 분광 특성과 기하 오차를 보완하기 위해, Domain Style Prompt로 전정색 영상의 특성을 반영하고 Mapping Network를 통해 공간 정렬을 수행
* 항공정사영상의 기하 정확도를 유지하면서도 전정색 영상의 도메인 특성을 반영한 '기준데이터'를 생성
    * 항공 영상의 좌표계를 유지한 채, 초소형 전정색 영상의 도메인 특성이 자연스럽게 반영된 기준데이터 생성
* 생성된 기준데이터의 유효성을 자기지도 학습 기반 정합 네트워크로 정량 검증
    * 대응되는 패치 쌍을 추출하고, Binary pseudo-label(정합 여부)과 Bias pseudo-label(중심점 위치 오프셋)을 생성

## Papers with code
<!-- 줄 바꿈은 문장 끝 스페이스바 두번 -->

### Pan-sharpening
| Venue | Year | AKA | Paper | GitHub |
|-------|------|-----|--------|--------|
| AAAI | 2025 | MFFA | [Wavelet-Assisted Multi-Frequency Attention Network for Pansharpening](https://ojs.aaai.org/index.php/AAAI/article/view/32381) | [Link](https://github.com/Jie-1203/WFANet) |
| TGRS | 2025 | CDFInet | [Contour-Aware Dynamic Low-High Frequency Integration for Pan-Sharpening](https://ieeexplore.ieee.org/abstract/document/10909324) | [Link](https://github.com/Xidian-AIGroup190726/CDFInet) |
| TMM | 2025 | DUN | [Rethinking the Role of Panchromatic Images in Pan-sharpening](https://ieeexplore.ieee.org/abstract/document/10878451) | [Link](https://github.com/jiaming-wang/Project) |
| CVPR | 2024 | CANNet | [Content-Adaptive Non-Local Convolution for Remote Sensing Pansharpening](https://arxiv.org/abs/2404.07543) | [Link](https://github.com/duanyll/CANConv) |
| AAAI | 2024 | DISPNet | [Deep Unfolded Network with Intrinsic Supervision for Pan-Sharpening](https://ojs.aaai.org/index.php/AAAI/article/view/28350) | [Link](https://github.com/Baixuzx7/DISPNet) |
| AAAI | 2024 | FAME | [Frequency-Adaptive Pan-Sharpening with Mixture of Experts](https://ojs.aaai.org/index.php/AAAI/article/view/27984) | [Link](https://github.com/alexhe101/FAME-Net) |
| TPAMI | 2024 | SFINet | [A General Spatial-Frequency Learning Framework for Multimodal Image Fusion](https://ieeexplore.ieee.org/abstract/document/10443302) | [Link](https://github.com/manman1995/Awaresome-pansharpening) |
| GRSM | 2024 | Survey | [Hyperspectral Pansharpening: Critical review, tools, and future perspectives](https://ieeexplore.ieee.org/abstract/document/10804644) |  |
| TNNLS | 2024 | VOGTNET | [VOGTNet: Variational Optimization-Guided Two-Stage Network for Multispectral and Panchromatic Image Fusion](https://ieeexplore.ieee.org/document/10558848) | [Link](https://github.com/HZC-1998/VOGTNet) |
| TGRS | 2024 | UCGAN | [Unsupervised Pansharpening Based on Double-Cycle Consistency](https://ieeexplore.ieee.org/abstract/document/10457556) | [Link](https://github.com/zhysora/UCGAN) |
| IJCB | 2024 | DCINN | [A General Paradigm with Detail-Preserving Conditional Invertible Network for Image Fusion](https://link.springer.com/article/10.1007/s11263-023-01924-5) | [Link](https://github.com/wwhappylife/DCINN) |
| TGRS | 2024 | MFT-GAN | [MFT-GAN: A Multiscale Feature-Guided Transformer Network for Unsupervised Hyperspectral Pansharpening](https://ieeexplore.ieee.org/abstract/document/10531789) | [Link](https://github.com/liuofficial/MFT-GAN) |
| TGRS | 2024 | DCPNet | [DCPNet: A Dual-Task Collaborative Promotion Network for Pansharpening](https://ieeexplore.ieee.org/abstract/document/10473165) | [Link](https://github.com/lhf12278/DCPNet) |
| TGRS | 2024 | SDMSPan | [Supervised Detail-Guided Multiscale State-Space Model for Pan-Sharpening](https://ieeexplore.ieee.org/abstract/document/10812822) | [Link](https://github.com/zhaomengjiao123/SDMSPan) |
| TGRS | 2024 | PEMAE | [Pixel-Wise Ensembled Masked Autoencoder for Multispectral Pansharpening](https://ieeexplore.ieee.org/document/10649657) | [Link](https://github.com/yc-cui/PEMAE) |
|  |  |  |  |  |

<hr> <!-- 구분선 -->

### Remote Sensing
| Venue | Year | AKA | Paper | GitHub |
|-------|------|-----|--------|--------|
| TGRS | 2025 |  | [Brain-Inspired Online Adaptation for Remote Sensing With Spiking Neural Network](https://ieeexplore.ieee.org/abstract/document/10833809) | [Link](https://github.com/ThunderDavid/OASNN) |
| JSTARS | 2024 | Survey | [Multimodal Colearning Meets Remote Sensing: Taxonomy, State of the Art, and Future Works](https://ieeexplore.ieee.org/abstract/document/10474099) |  |
| IJCAI  | 2024 | DeepLightSR | [DeepLight: Reconstructing High-Resolution Observations of Nighttime Light With Multi-Modal Remote Sensing Data](https://arxiv.org/abs/2402.15659) | [Link](https://github.com/xian1234/DeepLight) |
| TGRS | 2024 | SFCoT | [Transferable Adversarial Attacks for Remote Sensing Object Recognition via SpatialFrequency Co-Transformation](https://github.com/fuyimin96/SFCo(https://ieeexplore.ieee.org/document/10636327) | [Link](https://github.com/fuyimin96/SFCoT) |
| TGRS | 2024 | GMFnet | [ConvGRU-Based Multiscale Frequency Fusion Network for PAN-MS Joint Classification](https://ieeexplore.ieee.org/abstract/document/10570233) | [Link](https://github.com/Xidian-AIGroup190726/GMFnet) |
|  |  |  |  |  |

<hr>

### I2I via Generative Models
| Venue | Year | AKA | Paper | GitHub |
|-------|------|-----|--------|--------|
| IGARSS | 2025 |  | [Fine-Tuning Adversarially-Robust Transformers for Single-Image Dehazing](https://arxiv.org/abs/2504.17829) | [Link](https://github.com/Vladimirescu/RobustDehazing) |
| TGRS | 2025 | SGLF | [Cross-Modality Domain Adaptation Based on Semantic Graph Learning: From Optical to SAR Images](https://ieeexplore.ieee.org/abstract/document/10963724) | [Link](https://github.com/XZhang878/SGLF) |
| TGRS | 2024 | DR-AVIT | [DR-AVIT: Toward Diverse and Realistic Aerial Visible-to-Infrared Image Translation](https://ieeexplore.ieee.org/abstract/document/10540003) | [Link](https://github.com/silver-hzh/DR-AVIT) |
|  |  |  |  |  |

