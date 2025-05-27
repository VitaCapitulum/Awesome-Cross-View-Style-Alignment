# Overview
This page outlines the research procedure and the required [template](https://www.overleaf.com/2777621724xcrtxfftdmty#9fd14f).  
The relevant research papers are available on [this](../README.md) page

## Key challenge
* 8bit 흑백 항공정사영상과 11bit 초소형 전정색 영상 간의 도메인 차이와 미세 기하학적 오차를 보정
    * 분광 특성과 기하 오차를 보완하기 위해, Domain Style Prompt로 전정색 영상의 특성을 반영하고 Mapping Network를 통해 공간 정렬을 수행
* 항공정사영상의 기하 정확도를 유지하면서도 전정색 영상의 도메인 특성을 반영한 '기준데이터'를 생성
    * 항공 영상의 좌표계를 유지한 채, 초소형 전정색 영상의 도메인 특성이 자연스럽게 반영된 기준데이터 생성
* 생성된 기준데이터의 유효성을 자기지도 학습 기반 정합 네트워크로 정량 검증
    * 대응되는 패치 쌍을 추출하고, Binary pseudo-label(정합 여부)과 Bias pseudo-label(중심점 위치 오프셋)을 생성

<hr>

### Background
#### Dataset
Many research papers utilize Gaofen-2(GF2), QuickBird(QB), and WorldView-3(WV3) in their studies. You can download a sample [PanCollection](https://github.com/liangjiandeng/PanCollection) or [PanBench](https://github.com/XavierJiezou/Pansharpening)

#### Example visualization of the WV3 train dataset(PanCollection)
GT : shape(9714, 8, 64, 64), min(0.0000), max(2047.0000)  
LMS : shape(9714, 8, 64, 64), min(-222.5743), max(2323.9167)  
MS : shape(9714, 8, 16, 16), min(25.4855), max(1997.7802)  
PAN :shape(9714, 1, 64, 64), min(76.4237), max(1988.2261)  
<p align="center">
  <img src="../fig/grid_0.png" style="width:100%;">
</p>  
<p align="center">
  <img src="../fig/grid_1.png" style="width:100%;">
</p>  
<p align="center">
  <img src="../fig/grid_2.png" style="width:100%;">
</p>  

#### Example visualization of the WV3 train dataset(PanBench)
PAN : 1024 x 1024  
NIR : 256 x 256  
RGB : 256 x 256  

<p align="center">
  <img src="../fig/PanBench_WV3.png" style="width:100%;">
</p> 

<hr>

#### Basic concepts
| Term | Explanation | Remarks |
|----|--------|----|
| PAN (Panchromatic) | 흑백 이미지로, 넓은 스펙트럼 범위를 하나의 밴드로 수집하여 높은 공간 해상도를 제공 |  |
| MS (Multispectral) | 여러 개의 스펙트럼 밴드를 가지며 중간 정도의 분광 해상도와 낮은 공간 해상도 |  |
| HSI (Hyperspectral Image) | 수십~수백 개의 분광 밴드를 가지는 고분광 이미지 |  |
| Spatial Resolution | 공간 해상도, 픽셀당 실제 지표의 크기 | 값이 낮을수록 해상도가 좋음 |
| Spectral Resolution | 분광 해상도, 수집 가능한 밴드 수와 스펙트럼 간격의 정밀도 | 값이 높을수록 더 세분화된 스펙트럼 정보 |
| Pansharpening | PAN + MS → 고해상도 다중분광 이미지 생성 |  |
| Hyper-pansharpening | PAN + HSI → 고해상도 고분광 이미지 생성 |  |
| Component Substitution (CS) | MS 이미지를 색상 성분 등으로 분해한 뒤, 그 중 하나를 PAN 이미지로 대체하여 공간 해상도 향상 | IHS, PCA, Brovey 등|
| Multiresolution Analysis (MRA) | PAN 이미지에서 다중 스케일 고주파 성분만 추출해서 MS 이미지에 더함 (고주파 → 공간 정보) | Wavelet, Contourlet 등 |
| Variational Optimization (VO) | 물리적/해석적 모델 기반의 역문제로 정식화 | Sparse Representation, Bayesian Inference 등 |
| ML/DL | 데이터 기반 함수 근사 문제로 학습, MS+PAN을 입력 → HRMS 등을 출력 | CNN, GAN, Transformer, Mamba, Diffusion |
|  |  |  |

