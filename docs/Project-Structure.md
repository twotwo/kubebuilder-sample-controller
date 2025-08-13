# 项目目录结构

## 核心目录

- `api/v1alpha1/` CRD类型定义
- `controllers/` 控制器业务逻辑
- `internal/billing/` 计费相关的核心实现
- `config/` 所有Kubernetes配置文件
- `docs` 项目文档
- `test/` 完整的测试体系

```bash
$ tree ../kubebuilder-sample-controller
../kubebuilder-sample-controller
├── api
│   └── v1alpha1
│       ├── expelorcs_types.go           # API版本信息
│       ├── groupversion_info.go         # CRD类型定义
│       └── zz_generated.deepcopy.go     # 自动生成的深拷贝代码
├── bin                                  # 编译后的二进制文件
├── cmd
│   └── main.go                          # 程序入口点
├── config
│   ├── crd
│   │   ├── bases
│   │   │   └── samplecontroller.github.com_expelorcs.yaml
│   │   ├── kustomization.yaml
│   │   └── kustomizeconfig.yaml
│   ├── default
│   │   ├── cert_metrics_manager_patch.yaml
│   │   ├── kustomization.yaml
│   │   ├── manager_metrics_patch.yaml
│   │   └── metrics_service.yaml
│   ├── manager
│   │   ├── kustomization.yaml
│   │   └── manager.yaml
│   ├── network-policy
│   │   ├── allow-metrics-traffic.yaml
│   │   └── kustomization.yaml
│   ├── prometheus
│   │   ├── kustomization.yaml
│   │   ├── monitor.yaml
│   │   └── monitor_tls_patch.yaml
│   ├── rbac
│   │   ├── expelorcs_admin_role.yaml
│   │   ├── expelorcs_editor_role.yaml
│   │   ├── expelorcs_viewer_role.yaml
│   │   ├── kustomization.yaml
│   │   ├── leader_election_role.yaml
│   │   ├── leader_election_role_binding.yaml
│   │   ├── metrics_auth_role.yaml
│   │   ├── metrics_auth_role_binding.yaml
│   │   ├── metrics_reader_role.yaml
│   │   ├── role.yaml
│   │   ├── role_binding.yaml
│   │   └── service_account.yaml
│   └── samples
│       ├── kustomization.yaml
│       └── samplecontroller_v1alpha1_expelorcs.yaml
├── Dockerfile                           # 容器镜像构建文件
├── docs
│   └── Project-Structure.md
├── go.mod
├── go.sum
├── hack
│   └── boilerplate.go.txt
├── internal
│   └── controller
│       ├── expelorcs_controller.go
│       ├── expelorcs_controller_test.go
│       └── suite_test.go
├── LICENSE
├── Makefile                             # 构建脚本
├── PROJECT                              # Kubebuilder项目配置
├── README.md
└── test
    ├── e2e
    │   ├── e2e_suite_test.go
    │   └── e2e_test.go
    └── utils
        └── utils.go
```
