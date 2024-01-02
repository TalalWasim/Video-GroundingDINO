# Video-GroundingDINO: Towards Open-Vocabulary Spatio-Temporal Video Grounding

[Syed Talal Wasim](https://talalwasim.github.io),
[Muzammal Naseer](https://muzammal-naseer.netlify.app/),
[Salman Khan](https://salman-h-khan.github.io/),
[Ming-Hsuan Yang](http://faculty.ucmerced.edu/mhyang/),
[Fahad Shahbaz Khan](https://scholar.google.es/citations?user=zvaeYnUAAAAJ&hl=en)


[![paper](https://img.shields.io/badge/arXiv-Paper-<COLOR>.svg)](https://arxiv.org/abs/2307.06947)
<hr />

> **Abstract:**
>*Video grounding aims to localize a spatio-temporal section in a video corresponding to an input text query. This paper addresses a critical limitation in current video grounding methodologies by introducing an Open-Vocabulary Spatio-Temporal Video Grounding task. Unlike prevalent closed-set approaches that struggle with open-vocabulary scenarios due to limited training data and predefined vocabularies, our model leverages pre-trained representations from foundational spatial grounding models. This empowers it to effectively bridge the semantic gap between natural language and diverse visual content, achieving strong performance in closed-set and open-vocabulary settings. Our contributions include a novel spatio-temporal video grounding model, surpassing state-of-the-art results in closed-set evaluations on multiple datasets and demonstrating superior performance in open-vocabulary scenarios. Notably, the proposed model outperforms state-of-the-art methods in closed-set settings on VidSTG (Declarative and Interrogative) and HC-STVG (V1 and V2) datasets. Furthermore, in open-vocabulary evaluations on HC-STVG V1 and YouCook-Interactions, our model surpasses the recent best-performing models by 4.26 m_vIoU and 1.83% accuracy, demonstrating its efficacy in handling diverse linguistic and visual concepts for improved video understanding.*

## Table of Contents
<!--ts-->
   * [News](#rocket-News)
   * [Overview](#overview)
   * [Visualization](#visualization)
   * [Codes](#codes)
   * [Citation](#citation)
   * [Acknowledgements](#acknowledgements)
<!--te-->

## :rocket: News
* **(January 2, 2024)** 
  * Paper released. Codes and models will be released soon.
<hr />


## Overview

<p align="center">
  <img alt="Overall Architecture" src="figs/main_arch.png" width="1200"/>
  <p align="center"><b>The overall architecture of Video-GroundingDINO:</b> We present our video grounding architecture. It consists of <b>vision and text encoders</b> that produce visual and textual features. A <b>cross-modality spatio-temporal encoder</b> which fuses information across spatial/temporal dimensions and visual/textual modalities. A <b>language guided query selction</b> module to initialize cross-modal queries. A <b>cross-modality spatio-temporal decoder</b> to decode queries while fusing information from visual/textual features. And finally <b>two prediction heads</b> to predict the bounding boxes per frame and the temporal tube.</p>
</p>

<hr />


<p align="center">
  <img alt="Performance Overview" src="figs/intro_fig.png" width="600"/>
  <p align="center"><b>Performance comparison</b> on conventional closed-set and open-vocabulary settings for the video grounding task. We compare our approach with TubeDETR and STCAT in supervised setting for VidSTG declarative/interrogative and HC-STVG V1, along with open-vocabulary evaluation on HC-STVG V1 and YouCook-Interactions datasets.</p>
</p>


## Visualization

<p align="center">
  <img alt="Visualization" src="figs/vis_figure.jpg" width="1200"/>
  <p align="center">Sample visualization for video grounding result on HC-STVG V1 for TubeDETR, STCAT and ours with the prompt <b>The man behind the shirtless man turns and squats</b>. We show bounding boxes for <span style="color:red">Ground-truth</span>, <span style="color:green">Closed-Set Supervised</span>, and <span style="color:yellow">Open-Vocabulary</span> results. Note how both TubeDETR and STCAT are close to the ground truth in the supervised setting (STCAT more so than TubeDETR), they cannot correctly ground the text properly in the open-vocabulary setting.</p>
</p>

## Codes

Codes and models will be released soon.


## Citation
If you find our work, this repository, or pretrained models useful, please consider giving a star :star: and citation.
```bibtex
@article{wasim2024video-groundingDINO,
    author    = {Wasim, Syed Talal and Naseer, Muzammal and Khan, Salman and Yang, Ming-Hsuan and Khan, Fahad Shahbaz},
    title     = {Video-GroundingDINO: Towards Open-Vocabulary Spatio-Temporal Video Grounding},
    journal   = {arxiv},
    year      = {2023},
}
```

## Contact
If you have any questions, please create an issue on this repository or contact at syed.wasim@mbzuai.ac.ae.

## Acknowledgements
Our code is based on [GroundingDINO](https://github.com/IDEA-Research/GroundingDINO), [TubeDETR](https://github.com/antoyang/TubeDETR) and [STCAT](https://github.com/jy0205/STCAT) repositories. We thank the authors for releasing their code. If you use our model, please consider citing these works as well.
