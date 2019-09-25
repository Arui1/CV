        .
        ├── 3rdparty
        │   ├── include
        │   │   ├── NvInfer.h
        │   │   └── NvInferPlugin.h
        │   └── lib
        │       ├── libnvinfer.so
        │       ├── libnvinfer.so.5
        │       ├── libnvinfer.so.5.1.5
        │       ├── libnvinfer_plugin.so
        │       ├── libnvinfer_plugin.so.5
        │       ├── libnvinfer_plugin.so.5.1.5
        │       ├── libnvparsers.so
        │       ├── libnvparsers.so.5
        │       └── libnvparsers.so.5.1.5
        ├── CMakeLists.txt
        ├── LICENSE
        ├── docker
        │   └── Dockerfile
        ├── example
        │   ├── CMakeLists.txt
        │   └── test_hades.cpp
        ├── images
        │   ├── file.txt
        │   ├── not_pulp.jpg
        │   ├── test_normal.jpg
        │   └── test_sexy.jpg
        ├── include
        │   └── infer_yellow.hpp
        ├── lib
        │   ├── libshadow.so
        │   └── libsm_hades_yellow_sdk.so
        ├── models
        │   ├── sm_yellow_1.tronmodel
        │   ├── sm_yellow_2.tronmodel
        │   └── sm_yellow_3.tronmodel
        └── 闪马智能内容审核开发手册.PDF

        $ mkdir build

        $ cd build

        $ cmake ..

        $ make

        $ ./build/test_hades models/sm_yellow_1.tronmodel \
                             models/sm_yellow_2.tronmodel \
                             models/sm_yellow_3.tronmodel


        {"confidences":[{"index":0,"score":0.543734610080719,"class":"normal","subclass":"normal"},                     {"index":2,"score":0.37931761145591738,"class":"sexy","subclass":"sexy"},{"index":1,"score":0.07694774866104126,"class":"pulp","subclass":"pulp"}]}
        {"confidences":[{"index":2,"score":0.9020416736602783,"class":"sexy","subclass":"sexy"},{"index":0,"score":0.053318582475185397,"class":"normal","subclass":"normal"},{"index":1,"score":0.04463980346918106,"class":"pulp","subclass":"pulp"}]}
