# PINet_PG
Code for our PG paper [Human Pose Transfer by Adaptive Hierarchical Deformation](http://cic.tju.edu.cn/faculty/likun/pg2020.pdf)

This is Pytorch implementation for pose transfer on DeepFashion dataset. The code is extramly borrowed from [Pose Transfer](https://github.com/tengteng95/Pose-Transfer). Thanks for their work!

# Requirement
* Python 3 <br>
* pytorch 1.2 <br>
* torchvision <br>
* numpy <br>
* scipy <br>
* scikit-image <br>
* pillow <br>
* pandas <br>
* tqdm <br>
* dominate <br>

# Data

Data preparation for images and keypoints can follow [Pose Transfer](https://github.com/tengteng95/Pose-Transfer)
Parsing data can be found from [baidu](https://pan.baidu.com/s/1Ic8sIY-eYhGnIoZdDlhgxA), password:abcd

# Test
You can directly download our test results from [baidu](https://pan.baidu.com/s/15tcKgRV12NGByIrr4qoqDw) (fetch code: abcd).<br>
Pre-trained checkpoint can be found from [baidu](https://pan.baidu.com/s/1Orvpt42lV-R2uzI-10q3_A) (fetch code: abcd) and put it in the folder (-->checkpoints-->fashion_PInet_PG).

Test by yourself <br>
python test.py --dataroot ./fashion_data/ --name fashion_PInet_PG --model PInet --phase test --dataset_mode keypoint --norm instance --batchSize 1 --resize_or_crop no --gpu_ids 0 --BP_input_nc 18 --no_flip --which_model_netG PInet --checkpoints_dir ./checkpoints --pairLst ./fashion_data/fasion-resize-pairs-test.csv --which_epoch latest --results_dir ./results
