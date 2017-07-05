# tensorflow_object_detection_create_coco_tfrecord
Convert coco dataset to tfrecord for the tensorflow detection API.
# Attention
1) For easy use of this script, Your coco dataset directory struture should like this :
```
    +Your coco dataset root
        +train2014
        +val2014
        +annotations
            -instances_train2014.json
            -instances_val2014.json
```
2) To use this script, you should download python coco tools from [coco website ](http://mscoco.org/dataset/#download) and make it.
After make, copy the pycocotools directory to the directory of this "create_coco_tf_record.py"
or add the pycocotools path to  PYTHONPATH of ~/.bashrc file.
**For convientient , I add pycocotools build in my computer to the project directory, you can use it with python3 directly. But if you use python2, build the python coco tool from [!coco](http://mscoco.org/dataset/#download) **

# Example usage:
```
    python create_coco_tf_record.py --data_dir=/path/to/your/coco/root/directory \
        --set=train \
        --output_path=/where/you/want/to/save/pascal.record
        --shuffle_imgs=True
```