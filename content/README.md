# Overview
This page outlines the research procedure and the required [template](https://www.overleaf.com/2777621724xcrtxfftdmty#9fd14f).  
The relevant research papers are available on [this](README.md) page

## Key challenge
* 8bit 흑백 항공정사영상과 11bit 초소형 전정색 영상 간의 도메인 차이와 미세 기하학적 오차를 보정
    * 분광 특성과 기하 오차를 보완하기 위해, Domain Style Prompt로 전정색 영상의 특성을 반영하고 Mapping Network를 통해 공간 정렬을 수행
* 항공정사영상의 기하 정확도를 유지하면서도 전정색 영상의 도메인 특성을 반영한 '기준데이터'를 생성
    * 항공 영상의 좌표계를 유지한 채, 초소형 전정색 영상의 도메인 특성이 자연스럽게 반영된 기준데이터 생성
* 생성된 기준데이터의 유효성을 자기지도 학습 기반 정합 네트워크로 정량 검증
    * 대응되는 패치 쌍을 추출하고, Binary pseudo-label(정합 여부)과 Bias pseudo-label(중심점 위치 오프셋)을 생성

## 
