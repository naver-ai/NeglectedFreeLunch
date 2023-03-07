## Neglected Free Lunch – Learning Image Classifiers Using Annotation Byproducts | [Paper](coming_soon.pdf)

Dongyoon Han<sup>1*</sup>, Junsuk Choe<sup>2*</sup>, Seonghyeok Chun<sup>3</sup>, John Joon Young Chung<sup>4</sup>

Minsuk Chang<sup>5</sup>, Sangdoo Yun<sup>1</sup>, Jean Y. Song<sup>6</sup>, Seong Joon Oh<sup>7&dagger;</sup>  

<sub>\* Equal contribution</sub> <sub>&dagger;</sub> <sub> Corresponding author </sub>

<sup>1</sup> <sub>NAVER AI LAB</sub> <sup>2</sup> <sub>Sogang University</sub> <sup>3</sup> <sub>Dante Company</sub> <sup>4</sup> <sub>University of Michigan</sub>  <sup>5</sup> <sub>NAVER AI LAB, currently at Google</sub>  <sup>6</sup> <sub>DGIST</sub>  <sup>7</sup> <sub>University of T&uuml;bingen</sub> 

Supervised learning of image classifiers distills human knowledge into a parametric model *f* through pairs of images and corresponding labels (*X*,*Y*). We argue that this simple and widely used representation of human knowledge neglects rich auxiliary information from the annotation procedure, such as the time-series of mouse traces and clicks. 

<p align=center>
<img src="https://user-images.githubusercontent.com/7447092/203720567-dc6e1277-84d2-439c-a9f8-879e31c04e6f.png" alt="imagenet-byproduct-sample" width=500px />
<p/>

Our insight is that such **annotation byproducts** *Z* provide approximate human attention that weakly guides the model to focus on the foreground cues, reducing spurious correlations and discouraging shortcut learning. 

We have created **ImageNet-AB** and **COCO-AB** to verify this:

* [ImageNet-AB (annotation byproducts)](https://hybridsupervision-image-net.s3.us-east-2.amazonaws.com/repository/imagenet_ab_v1_0.tar.gz) (Click to start downloading; 529MB)
* [COCO-AB (annotation byproducts)](https://hybridsupervision-coco.s3.us-east-2.amazonaws.com/hybridsup/coco_ab_v1_0.json) (Click to start downloading; 380MB)

They are ImageNet and COCO training sets enriched with sample-wise annotation byproducts, collected by replicating the respective original annotation tasks. 

We refer to the new paradigm of training models with annotation byproducts as **learning using annotation byproducts (LUAB)**. 

<p align=center>
<img src="https://user-images.githubusercontent.com/7447092/203721515-2aea133d-1a77-4463-8372-5f0e0dbe4d2d.png" alt="luab" width=500px />
<p/>

We show that a simple multitask loss for regressing *Z* together with *Y* already improves the generalisability and robustness of the learned models. Compared to the original supervised learning, LUAB does not require extra annotation costs.

### Dataloader for ImageNet-AB and COCO-AB

We provide example dataloaders for the annotation byproducts.

* Dataloader for ImageNet-AB: [imagenet_dataloader.ipynb](imagenet_dataloader.ipynb)
* Dataloader for COCO-AB: [coco_dataloader.ipynb](coco_dataloader.ipynb)


### Annotation tools for ImageNet and COCO

* Annotation tool for ImageNet: [github.com/naver-ai/imagenet-annotation-tool](https://github.com/naver-ai/imagenet-annotation-tool)
* Annotation tool for COCO: [github.com/naver-ai/coco-annotation-tool](https://github.com/naver-ai/coco-annotation-tool)

### License

```
MIT License

Copyright (c) 2023-present NAVER Cloud Corp.

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```

### Citing our work

```
Coming soon
```
