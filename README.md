# ApacheDeepLearning302
ApacheDeepLearning302 for ApacheCon Global 2021 - Apache Pulsar, Apache MXNet, Apache NiFi, Apache Flink, Apache Tika



# Run Server with 2 models

multi-model-server --start --models caffenet=https://s3.amazonaws.com/model-server/model_archive_1.0/caffenet.mar crepe=https://s3.amazonaws.com/model-server/model_archive_1.0/crepe.mar --mms-config server.config


# Test Classification

curl -X POST http://127.0.0.1:9999/predictions/crepe -F "data=[{\"review_title\":\"Inception is the best\",\"review\": \"great direction and story\"}]"

