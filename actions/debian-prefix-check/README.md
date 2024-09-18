# debian-prefix-check
检查PR中是否存在debian前缀的文件

# 白名单
```
debian/patches/*
debian/manpage.*
debian/*.manpages
debian/changelog
debian/copyright
debian/compat
debian/source/format
```

# 使用方法
```yaml
uses: reviews-team-test/ci-check-action/actions/debian-prefix-check@debian-check
```

# 输入输出
| 输入参数| 描述| 是否必须| 默认值|
|:---:|:---:|:---:|:---:|
| repo_name | 检测仓库名称 | false | ${{github.repository}} |


| 输出参数| 描述| 示例|
|:---:|:---:|:---:|
| isFail | 检查是否失败 | true |
| check_msg | 检查失败输出信息 | 检测到debian目录文件有变更: debian/test,debian/control |