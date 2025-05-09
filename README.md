# Awesome Domain Style Alignment

1. 8bit 흑백 항공정사영상과 11bit 초소형 전정색 영상 간의 도메인 차이와 미세 기하학적 오차를 보정
    * 분광 특성과 기하 오차를 보완하기 위해, Domain Style Prompt로 전정색 영상의 특성을 반영하고 Mapping Network를 통해 공간 정렬을 수행
2. 항공정사영상의 기하 정확도를 유지하면서도 전정색 영상의 도메인 특성을 반영한 '기준데이터'를 생성
    * 항공 영상의 좌표계를 유지한 채, 초소형 전정색 영상의 도메인 특성이 자연스럽게 반영된 기준데이터 생성
3. 생성된 기준데이터의 유효성을 자기지도 학습 기반 정합 네트워크로 정량 검증
    * 대응되는 패치 쌍을 추출하고, Binary pseudo-label(정합 여부)과 Bias pseudo-label(중심점 위치 오프셋)을 자동 생성

## Papers with code
<!-- 줄 바꿈은 문장 끝 스페이스바 두번 -->

### Pan-sharpening
| Venue | Year | AKA | Paper | GitHub |
|-------|------|-----|--------|--------|
| GRSM | 2024 | Survey | [Hyperspectral Pansharpening: Critical review, tools, and future perspectives](https://ieeexplore.ieee.org/abstract/document/10804644) |  |
| TNNLS | 2024 | VOGTNET | [VOGTNet: Variational Optimization-Guided Two-Stage Network for Multispectral and Panchromatic Image Fusion](https://ieeexplore.ieee.org/document/10558848) | [Link](https://github.com/HZC-1998/VOGTNet) |
| TGRS | 2024 | UCGAN | [Unsupervised Pansharpening Based on Double-Cycle Consistency](https://ieeexplore.ieee.org/abstract/document/10457556) | [Link](https://github.com/zhysora/UCGAN) |
| IJCB | 2024 | DCINN | [A General Paradigm with Detail-Preserving Conditional Invertible Network for Image Fusion](https://link.springer.com/article/10.1007/s11263-023-01924-5) | [Link](https://github.com/wwhappylife/DCINN) |
| TGRS | 2024 | MFT-GAN | [MFT-GAN: A Multiscale Feature-Guided Transformer Network for Unsupervised Hyperspectral Pansharpening](https://ieeexplore.ieee.org/abstract/document/10531789) | [Link](https://github.com/liuofficial/MFT-GAN) |
| TGRS | 2024 | DCPNet | [DCPNet: A Dual-Task Collaborative Promotion Network for Pansharpening](https://ieeexplore.ieee.org/abstract/document/10473165) | [Link](https://github.com/lhf12278/DCPNet) |
| TPAMI | 2024 | SFINet | [A General Spatial-Frequency Learning Framework for Multimodal Image Fusion](https://ieeexplore.ieee.org/abstract/document/10443302) | [Link](https://github.com/manman1995/Awaresome-pansharpening) |
| AAAI | 2024 | DISPNet | [Deep Unfolded Network with Intrinsic Supervision for Pan-Sharpening](https://ojs.aaai.org/index.php/AAAI/article/view/28350) | [Link](https://github.com/Baixuzx7/DISPNet) |
| Information Fusion | 2024 | ZS-Pan | [Zero-shot semi-supervised learning for pansharpening](https://www.sciencedirect.com/science/article/pii/S1566253523003172) | [Link](https://github.com/coder-qicao/ZS-Pan) |
|  |  |  |  |  |

<hr> <!-- 구분선 -->

### Geometirc Alignment
| Venue | Year | AKA | Paper | GitHub |
|-------|------|-----|--------|--------|
|  |  |  |  |  |

<hr>

### Remote Sensing
| Venue | Year | AKA | Paper | GitHub |
|-------|------|-----|--------|--------|
| JSTARS | 2024 | Survey | [Multimodal Colearning Meets Remote Sensing: Taxonomy, State of the Art, and Future Works](https://ieeexplore.ieee.org/abstract/document/10474099) |  |
| Information Fusion | 2024 | NCGLF2 | [NCGLF2 : Network combining global and local features for fusion of multisource remote sensing data](https://www.sciencedirect.com/science/article/pii/S1566253523005080) | [Link](https://github.com/renqi1998/NCGLF2) |
|  |  |  |  |  |

<hr>

### Diffusion based I2I
| Venue | Year | AKA | Paper | GitHub |
|-------|------|-----|--------|--------|
|  |  |  |  |  |
