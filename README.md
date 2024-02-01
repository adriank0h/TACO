For convenience, annotations are provided in COCO format. Check the metadata here:
http://cocodataset.org/#format-data

# Getting started

### Requirements 

To install the required python packages simply type
```
pip3 install -r requirements.txt

```
pip3 install git+https://github.com/philferriere/cocoapi.git#subdirectory=PythonAPI
```

### Download

To download the dataset images simply issue
```
python3 download.py
```
**Unofficial data**

Annotations submitted via our website are added weekly to `data/annotations_unofficial.json`. 
You can use the same command to download the respective images:
```
python3 download.py --dataset_path ./data/annotations_unofficial.json
```

### Trash Detection

The implementation of [Mask R-CNN by Matterport](https://github.com/matterport/Mask_RCNN)  is included in ``/detector``
with a few modifications. Requirements are the same. Before using this, the dataset needs to be split. 
```
python3 split_dataset.py --dataset_dir ../data
```
