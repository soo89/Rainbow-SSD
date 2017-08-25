# Enhancement of SSD by concatenating feature maps for object detection

By [Jisoo Jeong](http://mipal.snu.ac.kr/index.php/Jisoo_Jeong), [Hyojin Park](http://mipal.snu.ac.kr/index.php/Hyojin_Park), [Nojun Kwak](http://mipal.snu.ac.kr/index.php/Nojun_Kwak)

## Intoroduction

<p align="center">
<img src="image/compared.png" alt="SSD Images vs R-SSD Images" width="1000px">
</p>

#### The conventional [SSD](https://github.com/weiliu89/caffe/tree/ssd) has a couple of points to be supplemented
   * Each layer in the feature pyramid is used independently (the same object can be detected in multiple scales)
   * Small objects are not detected well (this is not the problem only for SSD)


#### We tackle this problems as follows
   * The classifier network is implemented considering the relationship between layers in the feature pyramid
   * The number of channels in a layer is increased efficiently
   * The proposed network is suitable for sharing weights in the classifer network for different scales, resulting in a single classifier network


#### For more details, please refer to our [arXiv paper](https://arxiv.org/abs/1705.09587)


## Citing R-SSD

Please cite R-SSD in your publications if it helps your research

	@article{jeong2017enhancement,
	  title={Enhancement of SSD by concatenating feature maps for object detection},
	  author={Jeong, Jisoo and Park, Hyojin and Kwak, Nojun},
	  journal={arXiv preprint arXiv:1705.09587},
	  year={2017}
	}

## Installation & Preparation
We experimented with R-SSD using the SSD framework. To use our model, complete the installation & preparation on the [SSD homepage](https://github.com/weiliu89/caffe/tree/ssd)

## Models

Pascal VOC model 
   * [R-SSD300](https://drive.google.com/file/d/0B1gBZEl4EBWZUl95aHkyQlBkUWc/view?usp=sharing)
   * [R-SSD512](https://drive.google.com/file/d/0B1gBZEl4EBWZcFUydTI5NjhnRVk/view?usp=sharing)
   * [R-SSD300 with unified model](https://drive.google.com/file/d/0B1gBZEl4EBWZcU84dERNWkRNNms/view?usp=sharing)


To test this model, check "sh" file
  ```Shell
  # check your path in shell script (.sh file)
  # cd /home/soo/caffe_ssd -> cd /your/path
  ./R_SSD_300model_32.sh  (in file folder)
  ```

