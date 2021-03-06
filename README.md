# AFNet
Code for paper in CVPR2019, 'Attentive Feedback Network for Boundary-aware Salient Object Detection', Mengyang Feng, [Huchuan Lu](http://ice.dlut.edu.cn/lu/publications.html) and Errui Ding. [[google drive](https://drive.google.com/open?id=1EVZR8cNGUv3zb7JtR1fxbXZ8lp5mbgWe)] [[baidu yun](https://pan.baidu.com/s/1n-dRVC4sLWCmhhD5bnVXqg
)]

__Contact__:  Mengyang Feng, Email: mengyang_feng@mail.dlut.edu.cn

![AFNet pipline](https://github.com/ArcherFMY/AFNet/blob/master/figures/pipeline.png "pipline")

__Abstract__
Recent deep learning based salient object detection methods achieve gratifying performance built upon Fully Convolutional Neural Networks (FCNs). However, most of them have suffered from the boundary challenge. The state-of-the-art methods employ feature aggregation technique and can precisely find out wherein the salient object, but they often fail to segment out the entire object with fine boundaries, especially those raised narrow stripes. So there is still a large room for improvement over the FCN based models. In this paper, we design the Attentive Feedback Modules (AFMs) to better explore the structure of objects. A Boundary-Enhanced Loss (BEL) is further employed for learning exquisite boundaries. Our proposed deep model produces satisfying results on the object boundaries and achieves state-of-the-art performance on five widely tested salient object detection benchmarks. The network is in a fully convolutional fashion running at a speed of 26 FPS and does not need any post-processing.

__pre-computed saliency maps__ [[google drive](https://drive.google.com/file/d/1DztECdE-9HdpCll-XCUQUnkg5ul822P5/view?usp=sharing)] [[baidu yun](https://pan.baidu.com/s/1ywXgqq7yLcupr9o2RzRkgg)] (Fetch Code: jjhs)
## Usage
1. Clone this repo into your computer
```bash
git clone https://github.com/ArcherFMY/AFNet.git
```
2. Cd to `AFNet/caffe`, follow the [official instructions](http://caffe.berkeleyvision.org/installation.html) to build caffe. We provide our make file `my-Makefile.config` in folder `AFNet/caffe`.

The code has been tested successfully on Ubuntu 14.04 with CUDA 8.0 and OpenCV 3.1.0

3. Make `matcaffe`
```
make matcaffe -j
```

4. Download pretrained caffemodel from [[google drive](https://drive.google.com/file/d/1It3Cb4B93enKYXc8hq1E5tdWrqne2eFo/view?usp=sharing)] or [[baidu yun](https://pan.baidu.com/s/1DkAM0om90XCKGlmPoi_Lzg)] (Fetch Code: sifm) and extract the .zip file under the root directory `AFNet/`. 

5. Put the test image in `AFNet/test-Image/` and run `test_AFNet.m` to get the saliency maps. The results will be saved in `AFNet/results/AFNet/`

## Performance Preview
Quantitative comparisons
![table2](https://github.com/ArcherFMY/AFNet/blob/master/figures/table2.png "table2")

Quanlitative comparisons
![fig5](https://github.com/ArcherFMY/AFNet/blob/master/figures/fig5.png "fig5")

The scores are computed using this [evaluation tool box](https://github.com/ArcherFMY/sal_eval_toolbox)

## Citation
```
@InProceedings{Feng_2019_CVPR,
   author = {Feng, Mengyang and Lu, Huchuan and Ding, Errui},
   title = {Attentive Feedback Network for Boundary-aware Salient Object Detection},
   booktitle = CVPR,
   year = {2019}
}
```