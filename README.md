# Apache Deep Learning 302

## ApacheDeepLearning302 for ApacheCon Global 2021 - Apache Pulsar, Apache MXNet, Apache NiFi, Apache Flink, Apache Tika



### Run Server with 2 models

```
multi-model-server --start --models caffenet=https://s3.amazonaws.com/model-server/model_archive_1.0/caffenet.mar crepe=https://s3.amazonaws.com/model-server/model_archive_1.0/crepe.mar --mms-config server.config
```

### Test Classification

```
curl -X POST http://127.0.0.1:9999/predictions/crepe -F "data=[{\"review_title\":\"Inception is the best\",\"review\": \"great direction and story\"}]"
```

### Stop server

```
multi-model-server --stop
```

### List Mac Cameras

```
ioreg | grep -i cam
system_profiler SPCameraDataType
```

### Resources

* https://github.com/awslabs/multi-model-server
* https://thomasdelteil.github.io/TextClassificationCNNs_MXNet/
* https://modelzoo.co/model/character-level-cnn-text-classification-gluon
* https://github.com/awslabs/multi-model-server/blob/master/examples/gluon_character_cnn/README.md
* https://gluon.mxnet.io/
* https://mxnet.apache.org/versions/1.8.0/get_started?platform=macos&language=python&processor=cpu&environ=pip&
* https://github.com/awslabs/multi-model-server/tree/master/examples/gluon_character_cnn
* https://github.com/awslabs/multi-model-server/blob/master/examples/gluon_character_cnn/synset.txt
* https://github.com/deepjavalibrary/djl/tree/master/examples
* https://mxnet.apache.org/api/python/docs/api/gluon/model_zoo/index.html
* https://community.cloudera.com/t5/Community-Articles/Apache-Deep-Learning-101-Processing-Apache-MXNet-Model/ta-p/247944
* https://github.com/awslabs/multi-model-server/blob/master/docs/server.md  
* https://github.com/awslabs/multi-model-server/blob/master/docs/model_zoo.md 
