# kubebuilder-sample-controller
This Controller is developed by Kubebuilder v4.7.1

打破 K8s 知识垄断，将业务逻辑融入云原生！

## Purpose
推进 **adr-001 构建标准化业务控制面**，演示如何使用 Kubebuilder 开发控制器。

在 Pod 创建与释放时，根据定义的回调地址，发送通知给外部接口。

## Running
Clone source code

```shell
$ git clone git clone https://github.com/twotwo/kubebuilder-sample-controller.git
$ cd kubebuilder-sample-controller
```

Run localy

```shell
$ make install
$ make run
$ kubectl apply -f config/samples/samplecontroller_v1alpha1_expelorcs.yaml
```

Run container as Deployment

```shell
$ make install
$ make deploy
$ kubectl apply -f config/samples/samplecontroller_v1alpha1_expelorcs.yaml
```

## Reference

* [发现团队中的 Ork](https://www.xiaohongshu.com/explore/68905fca000000000200150d?xsec_token=ABpmCRDVIsw44zAU-x8bjA6Q7fsUSoQ3iaDW4oO4SmN6M)
* [项目目录结构](./docs/Project-Structure.md)
* [控制器规格说明书](./docs/CRD-Spec-v1.md)
