---
title: Troubleshooting
---

## I can't access some resources when installing Karmada

- Pull images from Google Container Registry (k8s.gcr.io).

  You can run the following commands to change the image registry in Mainland China.

  ```shell
  sed -i'' -e "s#k8s.gcr.io#registry.aliyuncs.com/google_containers#g" artifacts/deploy/karmada-etcd.yaml
  sed -i'' -e "s#k8s.gcr.io#registry.aliyuncs.com/google_containers#g" artifacts/deploy/karmada-apiserver.yaml
  sed -i'' -e "s#k8s.gcr.io#registry.aliyuncs.com/google_containers#g" artifacts/deploy/kube-controller-manager.yaml
  ```

- Download the Golang package in Mainland China and run the following command before installation.

  ```shell
  export GOPROXY=https://goproxy.cn
  ```