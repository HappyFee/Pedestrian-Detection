
文件格式

```
#评测文件
$/Cityscapes/shanshanzhang-citypersons/evaluation/eval_script/coco.py
$/Cityscapes/shanshanzhang-citypersons/evaluation/eval_script/eval_demo.py
$/Cityscapes/shanshanzhang-citypersons/evaluation/eval_script/eval_MR_multisetup.py

#注释文件
$/Cityscapes/shanshanzhang-citypersons/annotations
$/Cityscapes/shanshanzhang-citypersons/annotations/anno_train.mat
$/Cityscapes/shanshanzhang-citypersons/annotations/anno_val.mat
$/Cityscapes/shanshanzhang-citypersons/annotations/README.txt
#图片数据

$/Cityscapes/leftImg8bit/train/*
$/Cityscapes/leftImg8bit/val/*
$/Cityscapes/leftImg8bit/test/*
```

注释文件格式
```
CityPersons annotations
(1) data structure:
    one image per cell
    in each cell, there are three fields: city_name; im_name; bbs (bounding box annotations)

(2) bounding box annotation format:
　　 one object instance per row:
　　 [class_label, x1,y1,w,h, instance_id, x1_vis, y1_vis, w_vis, h_vis]

(3) class label definition:
　 class_label =0: ignore regions (fake humans, e.g. people on posters, reflections etc.)
    class_label =1: pedestrians
    class_label =2: riders
    class_label =3: sitting persons
    class_label =4: other persons with unusual postures
    class_label =5: group of people

(4) boxes:
　　visible boxes [x1_vis, y1_vis, w_vis, h_vis] are automatically generated from segmentation masks;
      (x1,y1) is the upper left corner.
      if class_label==1 or 2
        [x1,y1,w,h] is a well-aligned bounding box to the full body ;
      else
        [x1,y1,w,h] = [x1_vis, y1_vis, w_vis, h_vis];
```
