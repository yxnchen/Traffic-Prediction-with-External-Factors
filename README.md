# Traffic Prediction with External Factors
A Collection of resources for traffic prediction with external factors.

## 📖 Contents
- [Papers](#papers)
- [Datasets](#datasets)
- [Tools](#tools)

## Papers

> 🌧️ - Meteorology, including weather conditions, temperature, wind speed etc
>
> 📅 - Holidays
>
> 🚧 - Events, including traffic accidents, social events and public activities
>
> 🏪 - POIs or Land features

- Before 2020

|Journal/<br>Conference|Title|Factors|Code|Data|
|:---|:-------|:------|:------:|:------:|
|SIGSPATIAL '15|Traffic prediction in a bike-sharing system [Paper](https://doi.org/10.1145/2820783.2820837) [Page](http://urban-computing.com/index-65.htm)|🌧️|[Code](http://urban-computing.com/data/Codes.zip)|[NYC, D.C. Bike](http://urban-computing.com/data/Data.zip)|
|IEEE TVT|Improving traffic flow prediction with weather information in connected cars: A deep learning approach [Paper](https://ieeexplore.ieee.org/document/7501574/)|🌧️|||
|IEEE TKDE|Citywide Traffic Volume Estimation Using Trajectory Data [Paper](https://ieeexplore.ieee.org/document/7676331)|🌧️🏪|||
|SIGSPATIAL '18|Bike Flow Prediction with Multi-Graph Convolutional Networks [Paper](https://doi.org/10.1145/3274895.3274896)|🌧️|[GraphCNN-Bike](https://github.com/Di-Chai/GraphCNN-Bike)|[NYC bike](https://www.citibikenyc.com/system-data)<br>[CHI Bike](https://www.divvybikes.com/system-data)<br>[NOAA NCEI](https://www.ncdc.noaa.gov/data-access)|
|KDD '18|Deep sequence learning with auxiliary information for traffic prediction [Paper](https://dl.acm.org/doi/10.1145/3219819.3219895)|🚧|[BaiduTraffic](https://github.com/JingqingZ/BaiduTraffic)|[Q-Traffic](https://aistudio.baidu.com/datasetdetail/177190)|
|AAAI '18|Deep multi-view spatial-temporal network for taxi demand prediction [Paper](https://dl.acm.org/doi/abs/10.5555/3504035.3504351)|🌧️📅|[DMVST-Net](https://github.com/huaxiuyao/DMVST-Net)|DiDi|
|IET ITS|Combining weather condition data to predict traffic flow: A GRU‐based deep learning approach [Paper](https://ietresearch.onlinelibrary.wiley.com/doi/10.1049/iet-its.2017.0313)|🌧️||PeMS<br>[NOAA](https://www.ncdc.noaa.gov/cdo-web/datasets)|
|IEEE MDM '19|Temporal Graph Convolutional Networks for Traffic Speed Prediction Considering External Factors [Paper](https://ieeexplore.ieee.org/document/8788749)|🌧️📅🏪||[PEMSD7,PEMSD4](https://doi.org/10.5281/zenodo.7816008)|
|KDD '19|UrbanFM: Inferring Fine-Grained Urban Flows [Paper](http://doi.acm.org/10.1145/3292500.3330646)|🌧️📅🚧|[UrbanFM](https://github.com/yoshall/UrbanFM)|[TaxiBJ](https://github.com/yoshall/UrbanFM/tree/master/data)<br>[HappyValley](heat.qq.com)|


- 2020

|Journal/<br>Conference|Title|Factors|Code|Data|
|:---|:-------|:------|:------:|:------:|
|TR_C|Evaluation and prediction of transportation resilience under extreme weather events: A diffusion graph convolutional approach [Paper](https://doi.org/10.1016/j.trc.2020.102619)|🌧️|[resilience_shenzhen](https://github.com/Charles117/resilience_shenzhen)|DiDi<br>[NCAR](https://pan.baidu.com/s/1v7FTyb2VpLghoFg86V4E5w)|
|IEEE TKDE|Flow prediction in spatio-temporal networks based on multitask deep learning [Paper](https://ieeexplore.ieee.org/document/8606218)|🌧️📅|[MDL(uno)](https://github.com/wanzhixiao/MDL)|[NYC Taxi](https://www1.nyc.gov/site/tlc/about/tlc-trip-record-data.page)|

- 2021

|Journal/<br>Conference|Title|Factors|Code|Data|
|:---|:-------|:------|:------:|:------:|
|WWW '21|Fine-Grained Urban Flow Prediction [Paper](https://dl.acm.org/doi/10.1145/3442381.3449792)|🌧️📅🚧🏪||[TaxiBJ](https://github.com/yoshall/UrbanFM/tree/master/data)<br>[HappyValley](heat.qq.com)|
|IEEE Access|AST-GCN: Attribute-augmented spatiotemporal graph convolutional network for traffic forecasting [Paper](https://ieeexplore.ieee.org/document/9363197/)|🌧️🏪|[AST-GCN](https://github.com/lehaifeng/T-GCN/AST-GCN)|[SZ_taxi](https://github.com/lehaifeng/T-GCN)|

- 2022

|Journal/<br>Conference|Title|Factors|Code|Data|
|:---|:-------|:------|:------:|:------:|
|Information Sciences|Spatial–temporal short-term traffic flow prediction model based on dynamical-learning graph convolution mechanism [Paper](https://doi.org/10.1016/j.ins.2022.08.080)|🌧️|[AST-GCN](https://github.com/lehaifeng/T-GCN/AST-GCN)|OpenITS<br>[METR-LA](https://github.com/liyaguang/DCRNN/tree/master/data)|

- 2023

|Journal/<br>Conference|Title|Factors|Code|Data|
|:---|:-------|:------|:------:|:------:|
|IEEE ISPDS '23|An urban traffic flow prediction approach integrating external factors based on deep learning and knowledge graph [Paper](https://ieeexplore.ieee.org/document/10235681/)|🌧️🏪||Luohu Shenzhen|
|Elsevier ESWA|Spatio-temporal graph mixformer for traffic forecasting [Paper](https://www.sciencedirect.com/science/article/pii/S0957417423007832?via%3Dihub)|🌧️(But not use in experiment)|[stgm](https://github.com/mouradost/stgm)|[PeMS-Bay](https://doi.org/10.1145/3459637.3482000)<br>[PeMSD7M](https://doi.org/10.24963/ijcai.2018/505)<br>[METR-LA](https://github.com/liyaguang/DCRNN)|
|IEEE TKDE|Forecasting Fine-Grained Urban Flows Via Spatio-Temporal Contrastive Self-Supervision [Paper](https://ieeexplore.ieee.org/document/9864246)|🌧️📅|[UrbanSTC](https://github.com/HaoQu59/UrbanSTC)|[TaxiBJ](https://github.com/HaoQu59/UrbanSTC/tree/main/data/P1)<br>[BikeNYC](https://www.citibikenyc.com/system-data)|
|ECAI 2023|WeaGAN: Weather-aware graph attention network for traffic prediction [Paper](https://ebooks.iospress.nl/doi/10.3233/FAIA230565)|🌧️|[WeaGAN](https://github.com/YuxiWANGcode/WeaGAN)|[PeMS](https://github.com/YuxiWANGcode/WeaGAN)<br>[OpenWeather](https://openweathermap.org/)|
|Physica A|Traffic flow prediction under multiple adverse weather based on self-attention mechanism and deep learning models [Paper](https://www.sciencedirect.com/science/article/pii/S0378437123005435?via%3Dihub)|🌧️||[PeMS](http://pems.dot.ca.gov/)<br>[MesoWest](https://mesowest.utah.edu/)|
|Elsevier KBS|Spatio-temporal fusion and contrastive learning for urban flow prediction [Paper](https://doi.org/10.1016/j.knosys.2023.111104)|🌧️📅||[TaxiBJ](https://github.com/HaoQu59/UrbanSTC/tree/main/data/P1)<br>[BikeNYC](https://www.citibikenyc.com/system-data)|

- 2024

|Journal/<br>Conference|Title|Model|Factors|Code|Data|
|:---|:-------|:------|:------:|:------:|:------:|
|IET ITS|Combining weather factors to predict traffic flow: A spatial‐temporal fusion graph convolutional network‐based deep learning approach [Paper](https://ietresearch.onlinelibrary.wiley.com/doi/10.1049/itr2.12401)|STFGCN|🌧️||[PEMSD4](http://pems.dot.ca.gov/)<br>[MesoWest](https://mesowest.utah.edu/)|
|Information Sciences|A multi-channel spatial-temporal transformer model for traffic flow forecasting [Paper](https://doi.org/10.1016/j.ins.2024.120648)|MC-STTM|🌧️🚧(But not use due to limited information)||[PEMS03](https://ojs.aaai.org/index.php/AAAI/article/view/3881)<br>[PEMS04](https://ojs.aaai.org/index.php/AAAI/article/view/3881)<br>[PEMS07](https://ojs.aaai.org/index.php/AAAI/article/view/3881)<br>[PEMS08](https://ojs.aaai.org/index.php/AAAI/article/view/3881)<br>[METR-LA](https://ojs.aaai.org/index.php/AAAI/article/view/5438)<br>[PEMS-BAY](https://ojs.aaai.org/index.php/AAAI/article/view/5438)|
|Scientific Reports|A multi‐feature spatial–temporal  fusion network for traffic flow  prediction [Paper](https://doi.org/10.1038/s41598-024-65040-1)|ATFEM|🌧️📅||Guizhou|
|Elsevier EAAI|A traffic-weather generative adversarial network for traffic flow prediction for road networks under bad weather [Paper](https://doi.org/10.1016/j.engappai.2024.109125)|TWeather-GAN|🌧️||[PeMS](http://pems.dot.ca.gov/)<br>[MesoWest](https://mesowest.utah.edu/)|

- 2025

*DiDi: Open datasets from [Didi Chuxing GAIA Initiative](http://outreach.didichuxing.com/research/opendata/en/), tracing the records of taxi drivers and passengers in cities, China. It seems it is not applicable now.*

## Datasets



## Tools
