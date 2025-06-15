

<p align="center">
    <h4 align="center"><a href="https://www.scitepress.org/PublicationsDetail.aspx?ID=8NUYceiSlzs=&t=1">📑 Article</a>  |  <a href="https://youtu.be/FNBMEUbM3r8">🎬 Video</a> |  <a href="https://docs.google.com/presentation/d/1qIYRXm3XpVhu2XLbClz6T3ly-d5_mXHE/edit#slide=id.p1">🎙️Talk</a>    </h4> 
</p>

## BEVSeg2GTA: Joint Vehicle Segmentation and Graph Neural Networks for Ego Vehicle Trajectory Prediction in Bird's-Eye-View




 Abstrct: Predicting the trajectory of the ego vehicle is a critical task for autonomous vehicles. Even though traffic regulations have defined boundaries, various behaviours of the agents in real-life situations introduce complexities that are hard to capture comprehensively. This has led to a rising curiosity in ego vehicle trajectory prediction based on learning techniques. In this paper, we introduce BEVSeg2GTA Bird's-Eye View Joint Vehicle Segmentation and Graph Neural Network Trajectory Prediction, a novel approach that aims to forecast trajectories by treating perception and trajectory prediction as interconnected elements of a single system. By integrating these tasks, we demonstrate the possibility of improving perception accuracy and trajectory prediction error.  Initially, an encoder-decoder transformer-based deep network is employed to convert the multi-view camera images to a Bird's-Eye-View representation, followed by semantic segmentation of crucial agents, including the ego vehicle, other vehicles, and pedestrians within the scene.  Integrating a state-of-the-art backbone (such as EfficientNet) facilitates the extraction of strong features, which are used to construct a graph wherein a node represents each object within the scene.  Subsequently, the connections of these nodes are established by a $k$-Nearest Neighbours algorithm based on the distance metric.
Further, the node and image features are fed into a Graph Neural Network to learn the complex relationships between agents in a spatial context. Finally, the Graph Neural Network learned features are passed to a Spatio-Temporal Probabilistic Network to predict the ego vehicle's future trajectory accurately. The proposed framework, \textit{BEVSeg2GTA}, has been extensively evaluated on nuScenes datasets. The results demonstrate that the proposed method improves the state-of-the-art performance.

## Our Overview 📑
The BEVSeg2GTA framework aims to enhance ego vehicle trajectory prediction by integrating an encoder-decoder transformer and a GNN. The framework begins with a projection module, which transforms the input multi-camera views and map information into a BEV perspective using an encoder-decoder transformer. The segmentation output from this module is then fed into the GNN, which is utilized to construct a graph representing spatial information. This graph is subsequently employed as input into an STPN, which produces predictions of the ego vehicle's trajectory.

<img src="https://github.com/user-attachments/assets/ba98c000-debc-44a3-bc9b-2865923b900c" width ="850">



## Our Contribution  ⚙️


-  Our  proposal architecture (\textbf{BEVSeg2GTA}) offers an approach to accomplish vehicle segmentation and ego vehicle trajectory prediction tasks jointly, thereby achieving state-of-the-art results in both segmentation and trajectory prediction compared on the nuScenes dataset.
-  Our proposal integrates GNNs into the BEV architecture to capture the spatial relationships of the host vehicle and nearby objects, where the weights of the connections are inverses of the distances.
-  STPN is then integrated for trajectory estimation, so our network proposal considers both spatial and temporal aspects of the problem.


    

## Our proposed architecture ⛓️
Our proposed BEVSeg2GTA architecture:} Our method for jointly segmenting vehicles and predicting the trajectory of the ego vehicle consists of several stages. Initially, we extract image features across different scales and integrate a camera-aware positional embedding to address perspective distortion. Following this, we employ map-view positional embedding and cross-attention layers to gather contextual insights from various viewpoints and enhance the segmentation accuracy of the ego vehicle. The segmented results are then passed through a $k$NN to generate embeddings representing the surrounding environment. These embeddings are further utilized as input to a probabilistic layer for trajectory prediction, leveraging contextual information from the surrounding scene. Stars are used to indicate the novel contributions of this work (\textcolor{red}{red} and \textcolor{green}{green} indicating major and minor component contributions, respectively.

<img src="https://github.com/user-attachments/assets/f2287b30-3123-4085-8455-05eab78b23d1" width ="850">



    

## kNN Algorthim Analsis ⛓️
Our proposed BEVSeg2GTA architecture:} Our method for jointly segmenting vehicles and predicting the trajectory of the ego vehicle consists of several stages. Initially, we extract image features across different scales and integrate a camera-aware positional embedding to address perspective distortion. Following this, we employ map-view positional embedding and cross-attention layers to gather contextual insights from various viewpoints and enhance the segmentation accuracy of the ego vehicle. The segmented results are then passed through a $k$NN to generate embeddings representing the surrounding environment. These embeddings are further utilized as input to a probabilistic layer for trajectory prediction, leveraging contextual information from the surrounding scene. Stars are used to indicate the novel contributions of this work (\textcolor{red}{red} and \textcolor{green}{green} indicating major and minor component contributions, respectively.

<img src="https://github.com/user-attachments/assets/f2287b30-3123-4085-8455-05eab78b23d1" width ="850">


## Qualitative results 📈

 Qualitative results of BEVSeg2TP model for joint vehicle segmentation and ego vehicle trajectory prediction:} Six camera views around the vehicle (top three facing forward, bottom three facing backwards) with ground truth segmentation on the right. Our trajectory prediction with improved map-view segmentation (second from right) compared to the CVT  method (third from right).

<img src="https://github.com/sharmasushil/BEVSeg2TP/assets/70905483/e1796ce0-9cdb-4481-a3ed-5fbbff1acaef" width ="650">


## Citation 👇🏻
##### If you like our work, Please we kindly request that you cite the following paper:

```BibTeX
@conference{visapp24,
 author={Sushil Sharma. and Arindam Das. and Ganesh Sistu. and Mark Halton. and Ciarán Eising.},
 title={BEVSeg2TP: Surround View Camera Bird’s-Eye-View Based Joint Vehicle Segmentation and Ego Vehicle Trajectory Prediction},
 booktitle={Proceedings of the 19th International Joint Conference on Computer Vision, Imaging and Computer Graphics Theory and Applications - Volume 4: VISAPP},
 year={2024},
 pages={25-34},
 publisher={SciTePress},
 organization={INSTICC},
 doi={10.5220/0012321700003660},
 isbn={978-989-758-679-8},
 issn={2184-4321}}
 
```

