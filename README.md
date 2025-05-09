# Traffic Prediction with External Factors
A Collection of resources for traffic prediction with external factors apart from normal spatial (Network structure, connectivity) and temporal (Time-of-day, Day-in-week) features.

## 📖 Contents
- [Papers](#papers)
    - [Before 2020](#before-2020)
    - [2020](#2020)
    - [2021](#2021)
    - [2022](#2022)
    - [2023](#2023)
    - [2024](#2024)
    - [2025](#2025)
- [Datasets](#datasets)
- [Tools](#tools)

## Papers

- **Types of External Factor:**
> 🌧️ - Meteorology, including weather conditions, temperature, wind speed etc
>
> 📅 - Holidays or other temporal features
>
> 🚧 - Events, including traffic accidents, traffic conditions (congestion), social events and public activities
>
> 🏪 - POIs or Land features
>
> 🛣️ - Road or highway characteristics, e.g. link width, link length/distance, link type, number of lane, having bus stops, etc

- **Methods of Integrating External Factors**
> ➕ - Concatenation
>
> 📈 - LSTM, GRU
>
> 🔥 - Fusion
>
> 🟢 - Knowledge representation learning

### Before 2020

|Journal/<br>Conference|Title|Model|Factors|Code|Data|
|:---|:-------|:------|:------:|:------:|:------:|
|SIGSPATIAL '15|Traffic prediction in a bike-sharing system [Paper](https://doi.org/10.1145/2820783.2820837) [Page](http://urban-computing.com/index-65.htm)|based on GBRT|🌧️|[Code](http://urban-computing.com/data/Codes.zip)|[NYC, D.C. Bike](http://urban-computing.com/data/Data.zip)|
|IEEE TVT|Improving traffic flow prediction with weather information in connected cars: A deep learning approach [Paper](https://ieeexplore.ieee.org/document/7501574/)|based on DBNs, MTL|🌧️||[PeMS](http://pems.dot.ca.gov/)<br>[MesoWest](http://mesowest.utah.edu/)|
|IEEE TKDE|Citywide Traffic Volume Estimation Using Trajectory Data [Paper](https://ieeexplore.ieee.org/document/7676331)||🌧️🏪||Beijing|
|AAAI '17|Deep Spatio-Temporal Residual Networks for Citywide Crowd Flows Prediction [Paper](https://ojs.aaai.org/index.php/AAAI/article/view/10735) [Page](http://urban-computing.com/index-75.htm)|ST-ResNet|🌧️📅|[ST-ResNet-Pytorch](https://github.com/BruceBinBoxing/ST-ResNet-Pytorch)<br>[STResNet-PyTorch](https://github.com/KL4805/STResNet-PyTorch)<br>[ST-ResNet](https://github.com/topazape/ST-ResNet)<br>[STResNet](https://github.com/snehasinghania/STResNet)|[Beijing](https://github.com/topazape/ST-ResNet/tree/main/datasets/TaxiBJ)<br>[NYC](https://github.com/topazape/ST-ResNet/tree/main/datasets/BikeNYC)|
|SIGSPATIAL '18|Bike Flow Prediction with Multi-Graph Convolutional Networks [Paper](https://doi.org/10.1145/3274895.3274896)|Multi-Graph Convolutional Neural Network|🌧️|[GraphCNN-Bike](https://github.com/Di-Chai/GraphCNN-Bike)|[NYC bike](https://www.citibikenyc.com/system-data)<br>[CHI Bike](https://www.divvybikes.com/system-data)<br>[NOAA NCEI](https://www.ncdc.noaa.gov/data-access)|
|KDD '18|Deep sequence learning with auxiliary information for traffic prediction [Paper](https://dl.acm.org/doi/10.1145/3219819.3219895)|based on Seq2Seq+|🚧|[BaiduTraffic](https://github.com/JingqingZ/BaiduTraffic)|[Q-Traffic](https://aistudio.baidu.com/datasetdetail/177190)|
|IJCAI-18|GeoMAN: Multi-level Attention Networks for Geo-sensory Time Series Prediction [Paper](https://www.ijcai.org/proceedings/2018/476)|GeoMAN|🌧️🏪|[GeoMAN(Tensorflow)](https://github.com/yoshall/GeoMAN)<br>[GeoMAN(Pytorch)](https://github.com/xchadesi/GeoMAN)|Water quality<br>[Air quality](http://zx.bjmemc.com.cn/)|
|AAAI '18|Deep multi-view spatial-temporal network for taxi demand prediction [Paper](https://dl.acm.org/doi/abs/10.5555/3504035.3504351)|DMVST-Net|🌧️📅|[DMVST-Net](https://github.com/huaxiuyao/DMVST-Net)|DiDi(Guangzhou)|
|IET ITS|Combining weather condition data to predict traffic flow: A GRU‐based deep learning approach [Paper](https://ietresearch.onlinelibrary.wiley.com/doi/10.1049/iet-its.2017.0313)|DGRNN|🌧️||[PeMS](http://pems.dot.ca.gov/)<br>[NOAA](https://www.ncdc.noaa.gov/cdo-web/datasets)|
|IEEE MDM '19|Temporal Graph Convolutional Networks for Traffic Speed Prediction Considering External Factors [Paper](https://ieeexplore.ieee.org/document/8788749)|GTCN|🌧️📅🏪||[PEMSD7,PEMSD4](https://doi.org/10.5281/zenodo.7816008)|
|AAAI '19|Spatiotemporal Multi-Graph Convolution Network for Ride-Hailing Demand Forecasting [Paper](https://doi.org/10.1609/aaai.v33i01.33013656)|ST-MGCN|🏪|[ST-MGCN](https://github.com/underdoc-wang/ST-MGCN)|Beijing<br>Shanghai|
|AAAI '19|DeepSTN+: Context-Aware Spatial-Temporal Neural Network for Crowd Flow Prediction in Metropolis [Paper](https://doi.org/10.1609/aaai.v33i01.33011020)|DeepSTN+|🏪|[DeepSTN](https://github.com/FIBLAB/DeepSTN)|MobileBJ<br>[BikeNYC](https://www.citibikenyc.com/system-data)|
|AAAI '19|Revisiting Spatial-Temporal Similarity: A Deep Learning Framework for Traffic Prediction [Paper](https://doi.org/10.1609/aaai.v33i01.33015668)|STDN|🌧️🚧(But not use in experiment)|[STDN](https://github.com/tangxianfeng/STDN)|[NYC-Taxi](https://github.com/tangxianfeng/STDN)<br>[NYC-Bike](https://github.com/tangxianfeng/STDN)|
|KDD '19|UrbanFM: Inferring Fine-Grained Urban Flows [Paper](http://doi.acm.org/10.1145/3292500.3330646)|UrbanFM|🌧️📅🚧|[UrbanFM](https://github.com/yoshall/UrbanFM)|[TaxiBJ](https://github.com/yoshall/UrbanFM/tree/master/data)<br>[HappyValley](https://heat.qq.com)|
|KDD '19|Urban traffic prediction from spatio-temporal data using deep meta learning [Paper](https://doi.org/10.1145/3292500.3330884)|ST-MetaNet|🏪🛣️|[ST-MetaNet](https://github.com/panzheyi/ST-MetaNet)|[TDrive(flow)](http://urban-computing.com/index-58.htm)<br>[METR-LA(speed)](https://paperswithcode.com/dataset/metr-la)|


### 2020

|Journal/<br>Conference|Title|Model|Factors|Code|Data|
|:---|:-------|:------|:------:|:------:|:------:|
|AAAI '20|Multi-Range Attentive Bicomponent Graph Convolutional Network for Traffic Forecasting [Paper](https://doi.org/10.1609/aaai.v34i04.5758)|MRA-BGCN|🛣️|[MAR-BGCN_GPU_pytorch](https://github.com/wumingyao/MAR-BGCN_GPU_pytorch)|[METR-LA](https://paperswithcode.com/dataset/metr-la)<br>[PEMS-BAY](https://paperswithcode.com/dataset/pems-bay)|
|IET ITS|Multi‐step traffic speed prediction model with auxiliary features on urban road networks and its understanding [Paper](https://doi.org/10.1049/iet-its.2020.0284)|EGC-LSTM|🌧️📅🛣️||[Guiyang](https://tianchi.aliyun.com/competition/entrance/231598/introduction)<br>[NOAA](https://www.noaa.gov/)|
|TR_C|Evaluation and prediction of transportation resilience under extreme weather events: A diffusion graph convolutional approach [Paper](https://doi.org/10.1016/j.trc.2020.102619)|based on DCRNN and dynamic-capturing algorithm|🌧️|[resilience_shenzhen](https://github.com/Charles117/resilience_shenzhen)|DiDi<br>[NCAR](https://pan.baidu.com/s/1v7FTyb2VpLghoFg86V4E5w)|
|IEEE TKDE|Flow prediction in spatio-temporal networks based on multitask deep learning [Paper](https://ieeexplore.ieee.org/document/8606218)|MDL|🌧️📅|[MDL(uno)](https://github.com/wanzhixiao/MDL)|[NYC Taxi](https://www1.nyc.gov/site/tlc/about/tlc-trip-record-data.page)|
|IEEE TITS|DeepSTD: Mining Spatio-Temporal Disturbances of Multiple Context Factors for Citywide Traffic Flow Prediction [Paper](https://ieeexplore.ieee.org/document/8793226)|DeepSTD|🌧️📅🏪|[DeepSTD](https://github.com/zhengchuanpan/DeepSTD)|Xiamen<br>[DiDi(Chengdu)](https://github.com/zhengchuanpan/DeepSTD/tree/main/data)|
|CIKM '20|Deep Graph Convolutional Networks for Incident-Driven Traffic Speed Prediction [Paper](https://doi.org/10.1145/3340531.3411873)|DIGC-Net|🌧️🚧||[SFO](https://developer.here.com/)<br>[NYC](https://developer.here.com/)<br>[Yahoo Weather API](https://developer.yahoo.com/weather/)<br>|

### 2021

|Journal/<br>Conference|Title|Model|Factors|Code|Data|
|:---|:-------|:------|:------:|:------:|:------:|
|IEEE TITS|STNN: A Spatio-Temporal Neural Network for Traffic Predictions [Paper](https://ieeexplore.ieee.org/document/9142387)|STNN|🏪🛣️||[HK-KL, ST, TM](https://data.gov.hk/en-data/dataset/hk-td-sm_4-traffic-data-strategic-major-roads)|
|Applied Intelligence|A multi-mode traffic flow prediction method with clustering based attention convolution LSTM [Paper](https://doi.org/10.1007/s10489-021-02770-z)|CACLSTM|🌧️📅||TaxiBJ|
|Wiley JAT|The Prediction of Multistep Traffic Flow Based on AST-GCN-LSTM [Paper](https://doi.org/10.1155/2021/9513170)|AST-GCN-LSTM|🌧️🏪||Luohu(Shenzhen)|
|WWW '21|Fine-Grained Urban Flow Prediction [Paper](https://dl.acm.org/doi/10.1145/3442381.3449792)|STRN|🌧️📅🚧🏪||[TaxiBJ](https://github.com/yoshall/UrbanFM/tree/master/data)<br>[HappyValley](https://heat.qq.com)|
|IEEE TITS|Dynamic Spatial-Temporal Representation Learning for Traffic Flow Prediction [Paper](https://ieeexplore.ieee.org/document/9127874)|ATFM|🌧️📅|[ATFM](https://github.com/liulingbo918/ATFM)|[TaxiBJ](https://github.com/liulingbo918/ATFM/tree/master/data/TaxiBJ)<br>[BikeNYC](https://github.com/liulingbo918/ATFM/tree/master/data/BikeNYC)<br>[TaxiNYC](https://github.com/liulingbo918/ATFM/tree/master/data/TaxiNYC)|
|Elsevier EAAI|A flexible deep learning-aware framework for travel time prediction considering traffic event [Paper](https://www.sciencedirect.com/science/article/pii/S0952197621003390)|MC-Net|🚧||Beijing (from Amap)|
|IEEE Access|Hybrid Deep Spatio-Temporal Models for Traffic Flow Prediction on Holidays and Under Adverse Weather [Paper](https://ieeexplore.ieee.org/document/9612205)|CL-CN-G<br>CL-CNG<br>G-CN-CL|🌧️📅||[PeMS](http://pems.dot.ca.gov/)<br>[MesoWest](https://mesowest.utah.edu/)|
|IEEE Access|AST-GCN: Attribute-augmented spatiotemporal graph convolutional network for traffic forecasting [Paper](https://ieeexplore.ieee.org/document/9363197/)|AST-GCN|🌧️🏪|[AST-GCN](https://github.com/lehaifeng/T-GCN/AST-GCN)|[SZ_taxi](https://github.com/lehaifeng/T-GCN)|

### 2022

|Journal/<br>Conference|Title|Model|Factors|Code|Data|
|:---|:-------|:------|:------:|:------:|:------:|
|Elsevier NN|Exploiting dynamic spatio-temporal graph convolutional neural networks for citywide traffic flows prediction [Paper](https://doi.org/10.1016/j.neunet.2021.10.021)|GCN-DHSTNet|🌧️📅🚧||[TaxiBJ](https://github.com/TolicWang/DeepST)<br>[BikeNYC](https://www.kaggle.com/akkithetechie/new-york-city-bike-share-dataset)|
|Information Sciences|Spatial–temporal short-term traffic flow prediction model based on dynamical-learning graph convolution mechanism [Paper](https://doi.org/10.1016/j.ins.2022.08.080)|Loc-GCLSTM|🌧️||[OpenITS](http://www.openits.cn/)<br>[METR-LA](https://github.com/liyaguang/DCRNN/tree/master/data)|
|Transportmetrica B|DLW-Net model for traffic flow prediction under adverse weather [Paper](https://doi.org/10.1080/21680566.2021.2008280)|DLW-Net|🌧️||[Hefei(OpenITS)](http://www.openits.cn/)<br>[Sacramento(PeMS)](http://pems.dot.ca.gov/)<br>[MesoWest](https://mesowest.utah.edu/)|
|IEEE TKDE|Predicting Citywide Crowd Flows in Irregular Regions Using Multi-View Graph Convolutional Networks [Paper](https://ieeexplore.ieee.org/document/9139357)|MVGCN|🏪🛣️||[TaxiNYC](http://www.nyc.gov/html/tlc/html/about/trip_record_data.shtml)<br>[TaxiBJ](https://github.com/amirkhango/DeepST/tree/master/data/TaxiBJ)<br>[BikeDC](https://www.capitalbikeshare.com/system-data)<br>[BikeNYC](https://www.citibikenyc.com/system-data)|
|KeAi DCAN|Attention-based spatio-temporal graph convolutional network considering external factors for multi-step traffic flow prediction [Paper](https://www.sciencedirect.com/science/article/pii/S2352864821000675)|ABSTGCN-EF|📅🚧||[PeMS-LA](https://github.com/liyaguang/DCRNN)<br>[PeMS-Bay](https://github.com/liyaguang/DCRNN)|
|WSDM '22|ST-GSP: Spatial-temporal global semantic representation learning for urban flow prediction [Paper](https://doi.org/10.1145/3488560.3498444)|ST-GSP|🌧️📅|[STGSP](https://github.com/k51/STGSP)|[TaxiBJ](https://github.com/HaoQu59/UrbanSTC/tree/main/data/P1)<br>[BikeNYC](https://www.citibikenyc.com/system-data)|
|IEEE TITS|KST-GCN: A Knowledge-Driven Spatial-Temporal Graph Convolutional Network for Traffic Forecasting [Paper](https://ieeexplore.ieee.org/document/9681326)|KST-GCN|🌧️🏪|[KST-GCN](https://github.com/lehaifeng/T-GCN/tree/master/KST-GCN)|Luohu(Shenzhen)|
|Wiley JAT|Metro Traffic Flow Prediction via Knowledge Graph and Spatiotemporal Graph Neural Network [Paper](https://doi.org/10.1155/2022/2348375)|KGR-STGNN|🌧️🚧||BJMF15(Beijing)|

### 2023

|Journal/<br>Conference|Title|Model|Factors|Code|Data|
|:---|:-------|:------|:------:|:------:|:------:|
|IEEE ICCCNT '23|Traffic Prediction Using Auxiliary Information Based on Mlbsae-A Hybrid Deep Learning Framework [Paper](https://ieeexplore.ieee.org/document/10307220)|MLBSAE|🌧️📅🚧||PeMS|
|IEEE ISPDS '23|An urban traffic flow prediction approach integrating external factors based on deep learning and knowledge graph [Paper](https://ieeexplore.ieee.org/document/10235681/)|KR-EAR|🌧️🏪||Luohu(Shenzhen)|
|AAAI '23|Spatio-Temporal Meta-Graph Learning for Traffic Forecasting [Paper](https://doi.org/10.1609/aaai.v37i7.25976)|MegaCRN|🚧(Used for robustness analysis)|[MegaCRN](https://github.com/deepkashiwa20/MegaCRN)|[METR-LA](https://github.com/deepkashiwa20/MegaCRN/tree/main/METRLA)<br>[PEMS-BAY](https://github.com/deepkashiwa20/MegaCRN/tree/main/PEMSBAY)<br>[EXPY-TKY](https://github.com/deepkashiwa20/MegaCRN/tree/main/EXPYTKY)|
|Elsevier ESWA|Spatio-temporal graph mixformer for traffic forecasting [Paper](https://www.sciencedirect.com/science/article/pii/S0957417423007832?via%3Dihub)|STGM|🌧️(But not use in experiment)|[stgm](https://github.com/mouradost/stgm)|[PeMS-Bay](https://doi.org/10.1145/3459637.3482000)<br>[PeMSD7M](https://doi.org/10.24963/ijcai.2018/505)<br>[METR-LA](https://github.com/liyaguang/DCRNN)|
|IEEE TKDE|Forecasting Fine-Grained Urban Flows Via Spatio-Temporal Contrastive Self-Supervision [Paper](https://ieeexplore.ieee.org/document/9864246)|UrbanSTC|🌧️📅|[UrbanSTC](https://github.com/HaoQu59/UrbanSTC)|[TaxiBJ](https://github.com/HaoQu59/UrbanSTC/tree/main/data/P1)<br>[BikeNYC](https://www.citibikenyc.com/system-data)|
|ECAI 2023|WeaGAN: Weather-aware graph attention network for traffic prediction [Paper](https://ebooks.iospress.nl/doi/10.3233/FAIA230565)|WeaGAN|🌧️|[WeaGAN](https://github.com/YuxiWANGcode/WeaGAN)|[PeMS](https://github.com/YuxiWANGcode/WeaGAN)<br>[OpenWeather](https://openweathermap.org/)|
|Physica A|Traffic flow prediction under multiple adverse weather based on self-attention mechanism and deep learning models [Paper](https://www.sciencedirect.com/science/article/pii/S0378437123005435?via%3Dihub)|DHA|🌧️||[PeMS](http://pems.dot.ca.gov/)<br>[MesoWest](https://mesowest.utah.edu/)|
|Elsevier KBS|Spatio-temporal fusion and contrastive learning for urban flow prediction [Paper](https://doi.org/10.1016/j.knosys.2023.111104)|ST-FCL|🌧️📅||[TaxiBJ](https://github.com/HaoQu59/UrbanSTC/tree/main/data/P1)<br>[BikeNYC](https://www.citibikenyc.com/system-data)|
||Spatio-temporal graph convolution network based on multimodal feature fusion (基于多模态特征融合的时空图卷积网络) [Paper](https://github.com/yanganYNU/AFFGCN/blob/main/paper/AFFGCN_paper.pdf)|AFFGCN|🌧️|[AFFGCN](https://github.com/yanganYNU/AFFGCN)|[PEMSD4](https://github.com/guoshnBJTU/ASTGNN)<br>[PEMSD8](https://github.com/guoshnBJTU/ASTGNN)<br>[Iowa Atmospheric Observatory](http://mesonet.agron.iastate.edu/request/download.phtml)|
|CIKM '23|Mask- and Contrast-Enhanced Spatio-Temporal Learning for Urban Flow Prediction [Paper](https://doi.org/10.1145/3583780.3614958)|MC-STL|🌧️📅|[MCSTL](https://github.com/CodeZx6/MCSTL)|[TaxiBJ](https://github.com/CodeZx6/MCSTL/tree/main/data/TaxiBJ_P1)<br>[BikeNYC](https://github.com/CodeZx6/MCSTL/tree/main/data/BikeNYC)|
|Nature CIS|Integrating knowledge representation into traffic prediction: a spatial–temporal graph neural network with adaptive fusion features [Paper](https://link.springer.com/article/10.1007/s40747-023-01299-7)|KR-STGNN|🌧️🏪||[SZ-taxi](https://github.com/lehaifeng/T-GCN/tree/master/data)<br>SZ_POI<br>SZ_Weather|
|MDPI Electronics|HIT-GCN: Spatial-Temporal Graph Convolutional Network Embedded with Heterogeneous Information of Road Network for Traffic Forecasting [Paper](https://doi.org/10.3390/electronics12061306)|HIT-GCN|🌧️🏪||[SZ-taxi](https://github.com/lehaifeng/T-GCN/tree/master/data)<br>SZ_POI<br>SZ_Weather|
|IEEE TITS|A Deep Learning Approach for Long-Term Traffic Flow Prediction With Multifactor Fusion Using Spatiotemporal Graph Convolutional Network [Paper](https://ieeexplore.ieee.org/document/9875028)||🌧️||[Minnesota](https://www.dot.state.mn.us/)<br>[NOAA](https://www.ncei.noaa.gov/)|
|IEEE TVT|Unified Spatial-Temporal Neighbor Attention Network for Dynamic Traffic Prediction [Paper](https://ieeexplore.ieee.org/document/9903347)|USTAN|🌧️🏪||[PriTra](https://github.com/HunanUniversityZhuXiao/PrivateCarTrajectoryData)<br>TaxiBJ<br>[METR-LA](https://github.com/liyaguang/DCRNN)<br>[PEMS-BAY](https://github.com/liyaguang/DCRNN)<br>[POI](https://www.openstreetmap.org/)<br>[Waether](https://www.wunderground.com/)<br>[Event](https://www.calendarlabs.com/online-calendar/)|

### 2024

|Journal/<br>Conference|Title|Model|Factors|Code|Data|
|:---|:-------|:------|:------:|:------:|:------:|
|IET ITS|Combining weather factors to predict traffic flow: A spatial‐temporal fusion graph convolutional network‐based deep learning approach [Paper](https://ietresearch.onlinelibrary.wiley.com/doi/10.1049/itr2.12401)|STFGCN|🌧️||[PEMSD4](http://pems.dot.ca.gov/)<br>[MesoWest](https://mesowest.utah.edu/)|
|Information Sciences|A multi-channel spatial-temporal transformer model for traffic flow forecasting [Paper](https://doi.org/10.1016/j.ins.2024.120648)|MC-STTM|🌧️🚧(But not use due to limited information)||[PEMS03](https://ojs.aaai.org/index.php/AAAI/article/view/3881)<br>[PEMS04](https://ojs.aaai.org/index.php/AAAI/article/view/3881)<br>[PEMS07](https://ojs.aaai.org/index.php/AAAI/article/view/3881)<br>[PEMS08](https://ojs.aaai.org/index.php/AAAI/article/view/3881)<br>[METR-LA](https://ojs.aaai.org/index.php/AAAI/article/view/5438)<br>[PEMS-BAY](https://ojs.aaai.org/index.php/AAAI/article/view/5438)|
|Scientific Reports|A multi‐feature spatial–temporal fusion network for traffic flow prediction [Paper](https://doi.org/10.1038/s41598-024-65040-1)|ATFEM|🌧️📅||Guizhou|
|Elsevier EAAI|A traffic-weather generative adversarial network for traffic flow prediction for road networks under bad weather [Paper](https://doi.org/10.1016/j.engappai.2024.109125)|TWeather-GAN|🌧️||[PeMS](http://pems.dot.ca.gov/)<br>[MesoWest](https://mesowest.utah.edu/)|
|T&F SSCE|Short-term traffic flow prediction at isolated intersections based on parallel multi-task learning [Paper](https://doi.org/10.1080/21642583.2024.2316160)|MTL-fusion|📅||Nanhu(Jiaxing)|
|ACM CIKM '24|Empowering traffic speed prediction with auxiliary feature-aided dependency learning [Paper](https://doi.org/10.1145/3627673.3679909)|ARIAN|🌧️📅||[PeMS-D4](https://doi.org/10.5281/zenodo.7816008)<br>[PeMS-D8](https://doi.org/10.5281/zenodo.7816008)<br>Cityway|
|ACM CIKM '24|Seeing the Forest for the Trees: Road-Level Insights Assisted Lane-Level Traffic Prediction [Paper](https://doi.org/10.1145/3627673.3679600)|McgVAE|🛣️|[McgVAE](https://github.com/ShuhaoLii/McgVAE)|[PeMS(_F)](https://github.com/ShuhaoLii/McgVAE/tree/master/Datasets)<br>[HuaNan(Guangzhou)](https://github.com/ShuhaoLii/McgVAE/tree/master/Datasets)|
|Elsevier AI|Dual-track spatio-temporal learning for urban flow prediction with adaptive normalization [Paper](https://doi.org/10.1016/j.artint.2024.104065)|DualST|🌧️📅||[TaxiBJ](https://github.com/HaoQu59/UrbanSTC/tree/main/data/P1)<br>[BikeNYC](https://www.citibikenyc.com/system-data)|
|ACM TKDE|DeepMeshCity: A Deep Learning Model for Urban Grid Prediction [Paper](https://doi.org/10.1145/3652859)|DeepMeshCity|🌧️📅|[DeepMeshCity](https://github.com/ILoveStudying/DeepMeshCity)|[TaxiBJ](https://github.com/ILoveStudying/DeepMeshCity)<br>[BousaiTYO](https://github.com/deepkashiwa20/DeepCrowd)<br>[BousaiOSA](https://github.com/deepkashiwa20/DeepCrowd)|

### 2025

|Journal/<br>Conference|Title|Model|Factors|Code|Data|
|:---|:-------|:------|:------:|:------:|:------:|
|Scientific Reports|Traffic flow prediction based on spatial-temporal multi factor fusion graph convolutional networks [Paper](https://doi.org/10.1038/s41598-025-96801-1)|STFGCN|🌧️||[PEMS03](https://ojs.aaai.org/index.php/AAAI/article/view/3881)<br>[PEMS04](https://ojs.aaai.org/index.php/AAAI/article/view/3881)<br>[PEMS07](https://ojs.aaai.org/index.php/AAAI/article/view/3881)<br>[PEMS08](https://ojs.aaai.org/index.php/AAAI/article/view/3881)|
|Scientific Reports|An urban road traffic flow prediction method based on multi-information fusion [Paper](https://doi.org/10.1038/s41598-025-88429-y)|MIFPN|🌧️📅🏪||[SZ-taxi](https://github.com/lehaifeng/T-GCN/tree/master/data)<br>SZ_POI<br>SZ_Weather|
|Scientific Reports|Linear attention based spatiotemporal multi graph GCN for traffic flow prediction [Paper](https://doi.org/10.1038/s41598-025-93179-y)|LASTGCN|🌧️📅||[PEMSD4,PEMSD8](https://doi.org/10.5281/zenodo.7816008)<br>[NOAA](https://www.ncdc.noaa.gov/cdo-web/datasets)|
|Nature NCAA|ASTGCN for traffic flow prediction based on weather influence [Paper](https://doi.org/10.1007/978-981-97-7007-6_31)|WI-ASTGCN|🌧️||[PEMSD4,PEMSD8](https://doi.org/10.5281/zenodo.7816008)<br>[MesoWest](https://mesowest.utah.edu/)|
|Applied Soft Computing|MGC-DMF: A traffic flow forecasting method based on multi-graph spatio-temporal convolution and dynamic metric fusion with multi-source basic information [Paper](https://linkinghub.elsevier.com/retrieve/pii/S1568494625004892)|MGC-DMF|🌧️(Used for predictive performance stability analysis)|[MGC-DMF](https://github.com/charlotte404/MGC-DMF)|[PEMSD4](https://github.com/guoshnBJTU/ASTGNN)<br>[PEMSD8](https://github.com/guoshnBJTU/ASTGNN)<br>[SZ-taxi](https://github.com/lehaifeng/T-GCN)|
|T&F TPT|Short-term traffic flow prediction based on adaptive graph convolutional recurrent network under multi-factor fusion [Paper](https://doi.org/10.1080/03081060.2025.2498968)|EAG-LSTMA|🌧️📅🚧||[Longgang(SZ)](https://github.com/WisleyWang/2020HUAWEI-big-data-challenge)|
|IEEE TVT|Condition-Guided Urban Traffic Co-Prediction With Multiple Sparse Surveillance Data [Paper](https://ieeexplore.ieee.org/document/10528876)|CSTN|🏪🛣️||[NYC taxi](https://opendata.cityofnewyork.us/)<br>[NYC Bike](https://opendata.cityofnewyork.us/)<br>[NYC Accident](https://opendata.cityofnewyork.us/)<br>External factors|
|KDD '25|CausalMob: Causal Human Mobility Prediction with LLMs-derived Human Intentions toward Public Events [Paper](https://doi.org/10.1145/3690624.3709231)|CausalMob|🚧|[CausalMob](https://github.com/YangXiaojie1998/CausalMob)|Japan|
|Elsevier NN|Enhancing urban flow prediction via mutual reinforcement with multi-scale regional information [Paper](https://doi.org/10.1016/j.neunet.2024.106900)|MR-UFP|🌧️📅🏪|[Data-of-MR-UPF](https://github.com/CodeZx6/Data-of-MR-UPF)|[TaxiBJ](https://github.com/HaoQu59/UrbanSTC/tree/main/data/P1)<br>[BikeNYC](https://www.citibikenyc.com/system-data)<br>[Region category](https://github.com/CodeZx6/Data-of-MR-UPF)|


*DiDi: Open datasets from [Didi Chuxing GAIA Initiative](http://outreach.didichuxing.com/research/opendata/en/), tracing the records of taxi drivers and passengers in cities, China. It seems it is not applicable now.*

## Datasets

**Commonly used public datasets summary**
|Name|Mode|Type|🌧️|📅|🚧|🏪|🛣️|Links|
|:---|:---|:---|:---:|:---:|:---:|:---:|:---:|:---|
|Bike NYC|Bike|Flow|✔|✔||||[https://www.citibikenyc.com/system-data](https://www.citibikenyc.com/system-data)<br>[https://opendata.cityofnewyork.us/](https://opendata.cityofnewyork.us/)<br>[http://urban-computing.com/data/Data.zip](http://urban-computing.com/data/Data.zip)<br>[https://github.com/topazape/ST-ResNet/tree/main/datasets/BikeNYC](https://github.com/topazape/ST-ResNet/tree/main/datasets/BikeNYC)<br>[https://github.com/tangxianfeng/STDN](https://github.com/tangxianfeng/STDN)<br>[https://github.com/liulingbo918/ATFM/tree/master/data/BikeNYC](https://github.com/liulingbo918/ATFM/tree/master/data/BikeNYC)<br>[https://github.com/CodeZx6/MCSTL/tree/main/data/BikeNYC](https://github.com/CodeZx6/MCSTL/tree/main/data/BikeNYC)|
|Bike D.C.|Bike|Flow|✔|✔||||[http://urban-computing.com/data/Data.zip](http://urban-computing.com/data/Data.zip)|
|Bike CHI|Bike|Flow||✔||||[https://www.divvybikes.com/system-data](https://www.divvybikes.com/system-data)<br>Weather:[https://www.ncdc.noaa.gov/data-access](https://www.ncdc.noaa.gov/data-access)|
|TaxiBJ|Taxi|Flow|✔|✔||||[https://github.com/topazape/ST-ResNet/tree/main/datasets/TaxiBJ](https://github.com/topazape/ST-ResNet/tree/main/datasets/TaxiBJ)<br>[https://github.com/yoshall/UrbanFM/tree/master/data](https://github.com/yoshall/UrbanFM/tree/master/data)<br>[https://github.com/liulingbo918/ATFM/tree/master/data/TaxiBJ](https://github.com/liulingbo918/ATFM/tree/master/data/TaxiBJ)<br>[https://github.com/HaoQu59/UrbanSTC/tree/main/data/P1](https://github.com/HaoQu59/UrbanSTC/tree/main/data/P1)<br>[https://github.com/CodeZx6/MCSTL/tree/main/data/TaxiBJ_P1](https://github.com/CodeZx6/MCSTL/tree/main/data/TaxiBJ_P1)<br>[https://github.com/ILoveStudying/DeepMeshCity](https://github.com/ILoveStudying/DeepMeshCity)|
|Chengdu|Taxi|Flow|✔|✔||✔||[https://github.com/zhengchuanpan/DeepSTD/tree/main/data](https://github.com/zhengchuanpan/DeepSTD/tree/main/data)|
|Shenzhen|Taxi|Speed||✔||||[https://github.com/lehaifeng/T-GCN/tree/master/data](https://github.com/lehaifeng/T-GCN/tree/master/data)|
|NYC|Taxi|Flow|✔|✔|✔|||[https://www1.nyc.gov/site/tlc/about/tlc-trip-record-data.page](https://www1.nyc.gov/site/tlc/about/tlc-trip-record-data.page)<br>[https://opendata.cityofnewyork.us/](https://opendata.cityofnewyork.us/)<br>[https://github.com/tangxianfeng/STDN](https://github.com/tangxianfeng/STDN)<br>[https://github.com/liulingbo918/ATFM/tree/master/data/TaxiNYC](https://github.com/liulingbo918/ATFM/tree/master/data/TaxiNYC)<br>Accident:[https://opendata.cityofnewyork.us/](https://opendata.cityofnewyork.us/)|
|NYC|Taxi|OD Flow|✔|✔||||[https://github.com/liulingbo918/CSTN](https://github.com/liulingbo918/CSTN)|
|T-Drive|Taxi|Flow||✔||||[http://urban-computing.com/index-58.htm](http://urban-computing.com/index-58.htm)|
|Longgang(SZ)|Car|Flow|✔|✔|✔|||[https://github.com/WisleyWang/2020HUAWEI-big-data-challenge](https://github.com/WisleyWang/2020HUAWEI-big-data-challenge)|
|HappyValley|Crowd|Flow|✔|✔|✔|||[https://heat.qq.com](https://heat.qq.com)|
|Guiyang|Car|Time|✔|✔|||✔|[https://tianchi.aliyun.com/competition/entrance/231598/introduction](https://tianchi.aliyun.com/competition/entrance/231598/introduction)<br>Weather:[https://www.noaa.gov/](https://www.noaa.gov/)|
|BousaiTYO|Crowd|Flow<br>Density||✔||||[https://github.com/deepkashiwa20/DeepCrowd](https://github.com/deepkashiwa20/DeepCrowd)|
|BousaiOSA|Crowd|Density||✔||||[https://github.com/deepkashiwa20/DeepCrowd](https://github.com/deepkashiwa20/DeepCrowd)|
|METR-LA|Highway|Flow<br>Speed<br>Occupancy||✔||||[https://data.mendeley.com/datasets/s42kkc5hsw/1](https://data.mendeley.com/datasets/s42kkc5hsw/1)<br>[https://github.com/liyaguang/DCRNN](https://github.com/liyaguang/DCRNN)<br>[https://zenodo.org/records/5724362](https://zenodo.org/records/5724362)|
|PeMS-BAY|Highway|Flow<br>Speed<br>Occupancy||✔||||[https://github.com/liyaguang/DCRNN](https://github.com/liyaguang/DCRNN)<br>[https://zenodo.org/records/5724362](https://zenodo.org/records/5724362)|
|PeMS03<br>PeMS04<br>PeMS07<br>PeMS08<br><br>PeMS-D4<br>PeMS-D7<br>PeMS-D8|Highway|Flow<br>Speed<br>Occupancy||✔||||[https://zenodo.org/records/7816008](https://zenodo.org/records/7816008)<br>[https://github.com/guoshnBJTU/ASTGNN/tree/main/data](https://github.com/guoshnBJTU/ASTGNN/tree/main/data)<br>[https://github.com/VeritasYin/STGCN_IJCAI-18/tree/master/dataset](https://github.com/VeritasYin/STGCN_IJCAI-18/tree/master/dataset)<br>[https://github.com/VeritasYin/STGCN_IJCAI-18/issues/6](https://github.com/VeritasYin/STGCN_IJCAI-18/issues/6)<br>[https://github.com/jswang/stgat_traffic_prediction/tree/main/dataset](https://github.com/jswang/stgat_traffic_prediction/tree/main/dataset)<br>[https://data.mendeley.com/datasets/s42kkc5hsw/1](https://data.mendeley.com/datasets/s42kkc5hsw/1)<br>[https://github.com/liangzhehan/DMSTGCN](https://github.com/liangzhehan/DMSTGCN)<br>[]()<br>Sometimes split to PeMS-D7(M) and PeMS-D7(L)|
|EXPY-TKY|Highway|||✔||||[https://github.com/deepkashiwa20/MegaCRN/tree/main/EXPYTKY](https://github.com/deepkashiwa20/MegaCRN/tree/main/EXPYTKY)|
|Meteorology||Weather<br>Wind<br>Temperature<br>...|✔|||||Meteorological data:<br>MOAA:[https://www.ncdc.noaa.gov/data-access](https://www.ncdc.noaa.gov/data-access)<br>MesoWest:[https://mesowest.utah.edu/](https://mesowest.utah.edu/)<br>OpenWeather:[https://openweathermap.org/](https://openweathermap.org/)<br>Iowa Atmospheric Observatory:[http://mesonet.agron.iastate.edu/request/download.phtml](http://mesonet.agron.iastate.edu/request/download.phtml)<br>Open-Meteo:[https://github.com/open-meteo/open-meteo](https://github.com/open-meteo/open-meteo)|
|Beijing|Metro|Inflow<br>Outflow|✔|✔||||[https://github.com/JinleiZhangBJTU/ResNet-LSTM-GCN/tree/master/data](https://github.com/JinleiZhangBJTU/ResNet-LSTM-GCN/tree/master/data)|
|Shanghai<br>Hangzhou|Metro|Inflow<br>Outflow||✔||||[https://github.com/ivechan/PVCGN/tree/master/data](https://github.com/ivechan/PVCGN/tree/master/data)<br>[https://doi.org/10.57760/sciencedb.09286](https://doi.org/10.57760/sciencedb.09286)<br>Raw HZ data:[https://tianchi.aliyun.com/competition/entrance/231708/introduction](https://tianchi.aliyun.com/competition/entrance/231708/introduction)or[https://cstr.cn/16666.11.nbsdc.pbNr124O](https://cstr.cn/16666.11.nbsdc.pbNr124O)|
|SHMOD<br>HZMOD|Metro|OD flow||✔||||[https://github.com/HCPLab-SYSU/HIAM](https://github.com/HCPLab-SYSU/HIAM)<br>Raw HZ data:[https://tianchi.aliyun.com/competition/entrance/231708/introduction](https://tianchi.aliyun.com/competition/entrance/231708/introduction)or[https://cstr.cn/16666.11.nbsdc.pbNr124O](https://cstr.cn/16666.11.nbsdc.pbNr124O)|
|Shenzhen|Metro|IC Card||✔||||Raw data:[https://cstr.cn/16666.11.nbsdc.l9I55m7P](https://cstr.cn/16666.11.nbsdc.l9I55m7P)|

## Tools
