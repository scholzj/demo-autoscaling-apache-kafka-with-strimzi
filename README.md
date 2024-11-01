# Autoscaling Apache Kafka with Strimzi

This repository contains files for auto-scaling Apache Kafka clusters with Strimzi and Kubernetes Horizontal Pod Autoscaling.
It is using tiered storage with NFS volume.
You might need to adjust it to use whatever you have available (object storage etc.)

_IMPORTANT:_
_This demo is based on Strimzi 0.44.0._
_It will not work with older Strimzi versions._
_For use with newer Strimzi versions, you might need to create a new container image with tiered storage plugins._

## Demo video

[![Alt text](https://img.youtube.com/vi/b8JZpom-67I/0.jpg)](https://www.youtube.com/watch?v=b8JZpom-67I)
