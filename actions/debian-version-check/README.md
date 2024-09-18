# debian-version-check
检查PR中deian/changelog文件变动，有则对比最新的2个版本是否设置正确

# 使用方法
```yaml
uses: reviews-team-test/ci-check-action/actions/debian-version-check@debian-check
```

# 输入输出
| 输入参数| 描述| 是否必须| 默认值|
|:---:|:---:|:---:|:---:|
| repo_name | 检测仓库名称 | false | ${{github.repository}} |


| 输出参数| 描述| 示例|
|:---:|:---:|:---:|
| isFail | 检查是否失败 | true |
| check_msg | 检查失败输出信息 | debian/changelog版本变动异常:6.0.58|6.0.58 |