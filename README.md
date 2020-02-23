# MXNet2Caffe: Convert MXNet model to Caffe model

You are welcome to file issues either for bugs in the source code, feature requests!


# Requirement:

conda,
MXNet, >=1.4
Caffe,


Step1: Given a MXNet Model, MXNet2Caffe can automatically generate both `.prototxt` and `.caffemodel`.

Step2: 
   1) config json2prototxt, open it and change TODO
   2) prototxt_basic.py   , open it and change TODO
#Before starting using MXNet2Caffe, you need to manually set the path in `find_caffe.py` and `find_mxnet.py`.

Step3: `python json2prototxt.py` to generate the corresponding `.prototxt`.

Step4: `python mxnet2caffe.py` to generate the corresponding `.caffemodel`.


## TODO

[1] Since their is not `Flaten` layer in caffe, you have to manually moidify the automatically generated `.prototxt`. In other words, you have to change the `bottom` of the layer just after the `Falatten` layer making it linking to the layer before the `Falatten` layer. Currently, this part has to be done manually.

[2] The converted model performances a little bit worse than the original MXNet model.

[3] Code for automatically reversing the weight (and bias) of the first layer to support BGR input.

[4] Better support for caffe's in-place feature.

[5] Several TODOs in `prototxt_basic.py`
