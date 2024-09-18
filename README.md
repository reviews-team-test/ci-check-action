# debianCheck
Debian检查总入口，触发debian检查的各个模块，对结果进行汇总并生成评论文件，模块如下:
* debian-prefix-check: 检查PR中是否存在debian前缀的文件
* debian-version-check: 检查PR中是否deian/changelog版本是否正确
* debian-keys-check: 检查PR文件中是否存在指定敏感词设置

# 目录结构
```
.
├── actions
│   ├── debian-keys-check
│   │   ├── action.yml
│   │   └── debian-keys-check.py
│   ├── debian-prefix-check
│   │   └── action.yml
│   └── debian-version-check
│       └── action.yml
├── action.yml
└── README.md
```

# 使用方法
```yaml
uses: reviews-team-test/ci-check-action@debian-check
```

# 输入输出
| 输入参数| 描述| 是否必须| 默认值|
|:---:|:---:|:---:|:---:|
| repo_name | 检测仓库名称 | false | ${{github.repository}} |


| 输出参数| 描述| 示例|
|:---:|:---:|:---:|
| summary-status | Debian检查状态 | '否' |
| summary-result | Debian检查结果汇总 | '0\|0\|2' |