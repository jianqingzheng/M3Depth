## [Self-Supervised Depth Estimation in Laparoscopic Image using 3D Geometric Consistency](https://arxiv.org/abs/2208.08407) (MICCAI 2022)
By [Baoru Huang](https://baoru.netlify.app/), Jian-Qing Zheng, [Anh Nguyen](https://www.csc.liv.ac.uk/~anguyen), Chi Xu, Ioannis Gkouzionis, Kunal Vyas, David Tuch, Stamatia Giannarou, Daniel S. Elson

![image](https://github.com/br0202/M3Depth/blob/master/vis/frameworks.png "m3depth")

### Contents
1. [Requirements](#requirements)
2. [Training&Testing](#training)
3. [Notes](#notes)


### Requirements

1. Python version 3.8.5
2. Pytorch version: pytorch==1.6.0 torchvision==0.8.2 torchaudio==0.7.0 cudatoolkit=10.2.89
3. pytorch3d version 0.3.0
2. Cuda version 10.2

	
### Training & Testing

1. We train M3Depth on [SCARED](https://endovissub2019-scared.grand-challenge.org/)
	- We need to extract images from the videos and rectify the stereo image pairs with the given camera parameters (endoscope_calibration.yaml). 
	- Only keyframes were together with accurate depth maps. 
	- Sort the absolute image root and save them in `$splits/Endovis_origin/train_files.txt`.
	- Change the data directory to the folder of data.

2. Train M3Depth:
	- `cd $M3Depth`
	- `python main.py --mode train`
	
3. Test M3Depth:
    - `cd $M3Depth`
    - `python main.py --mode test`

4. Results
![image](https://github.com/br0202/M3Depth/blob/master/vis/quan_results.png "results")


### Citing 

If you find our paper useful in your research, please consider citing:

        @inproceedings{huang2022self,
          title={Self-supervised Depth Estimation in Laparoscopic Image Using 3D Geometric Consistency},
          author={Huang, Baoru and Zheng, Jian-Qing and Nguyen, Anh and Xu, Chi and Gkouzionis, Ioannis and Vyas, Kunal and Tuch, David and Giannarou, Stamatia and Elson, Daniel S},
          booktitle={International Conference on Medical Image Computing and Computer-Assisted Intervention},
          pages={13--22},
          year={2022},
          organization={Springer}
        }


### License
MIT License

### Acknowledgement
This repo used a lot of source code from [UPDATE_HERE](https://github.com/rbgirshick/UPDATE_LINK)
