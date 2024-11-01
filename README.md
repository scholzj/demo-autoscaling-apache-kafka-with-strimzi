# Autoscaling Apache Kafka with Strimzi

This repository contains files for auto-scaling Apache Kafka clusters with Strimzi and Kubernetes Horizontal Pod Autoscaling.
It is using tiered storage with NFS volume.
You might need to adjust it to use whatever you have available (S3, other object storage etc.)

_IMPORTANT:_
_This demo is based on Strimzi 0.44.0._
_It will not work with older Strimzi versions._
_For use with newer Strimzi versions, you might need to create a new container image with tiered storage plugins._

## Demo video

[![Alt text](https://img.youtube.com/vi/b8JZpom-67I/0.jpg)](https://www.youtube.com/watch?v=b8JZpom-67I)

## Execute the demo

To execute the demo, just deploy the files one-by-one.
After you deploy the [`04-load.yaml` file](./04-load.yaml) to create the load, you can just sit and wait for it to scale.
To scale-down, you should need just to delete the load.

The [`00-pvc.yaml` file] creates the NFS volume used for the tiered storage.
It expects that you have a storage class named `nfs` to create it.
You can replace it with your shared storage or object storage if needed.
For demonstration purposes, you can also use for example the [NFS Provisioner Operator](https://operatorhub.io/operator/nfs-provisioner-operator).