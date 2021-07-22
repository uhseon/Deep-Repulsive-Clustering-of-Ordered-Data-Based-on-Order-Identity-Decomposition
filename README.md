# Deep Repulsive Clustering of Ordered Data Based on Order-Identity Decomposition
Official TensorFlow Implementation of the ICLR 2021 paper, ["Deep Repulsive Clustering of Ordered Data Based on Order-Identity Decomposition."](https://openreview.net/pdf?id=Yz-XtK5RBxB)

## Requirements
- TensorFlow 2.0 or higher 
- python 3.7


## Pretrained Model and Reference List for Quick Start
- [Pre-trained model](https://drive.google.com/file/d/1GlsU8bS2LeDCuM0aE8A-AeqE6l3UlRfn/view?usp=sharing)
- [Reference list](https://drive.google.com/file/d/18cAlzj-_Kr8gFIYUzCmrgVXu8yjzLoMf/view?usp=sharing)


## Datasets
- [MORPH II](https://ebill.uncw.edu/C20231_ustores/web/classic/product_detail.jsp?PRODUCTID=8) 
- [Balanced](https://github.com/changsukim-ku/order-learning)


## Quick Start: Code Usage Example
1. Modify Config file 
- Adjust img_folder, train & test list for your purpose. As a default, MORPH setting A is used in the source code. 

2. Clustering ordered data by DRC-ORID
```
    $ cd train
    $ cd morph
    $ python train_kCH_morph_clustering.py
```    
- This will generate the centroids file and checkpoint of feature extractor. 

3. Get clustering results and train VGG-based network
```
    $ python get_clustering_info_setting_A.py
    $ python train_estimation_kCH_setting_A.py
```
4. Select references based on ORID results
```
    $ cd test
    $ python morph_ref_sel_kCH_by_attr_Setting_A.py
```
5. Run test
```
    $ python test_morph_kCH_by_attr_setting_A.py
```


## Cite

[DRC-ORID paper](https://openreview.net/pdf?id=Yz-XtK5RBxB):

```
@inproceedings{lee2021repulsive},
  title     = {Deep Repulsive Clustering of Ordered Data Based on Order-Identity Decomposition},
  author    = {Lee, Seon-Ho and Kim, Chang-Su},
  booktitle = {International Conference on Learning Representations},
  year      = {2021}
}
```
