# debian-keys-check
检查PR文件中是否存在指定敏感词设置

# 目录结构
```
.
├── action.yml
├── debian-keys-check.py
└── README.md
```

# 使用方法
```yaml
uses: reviews-team-test/ci-check-action/actions/debian-keys-check@debian-check
```

# 输入输出
| 输入参数| 描述| 是否必须| 默认值|
|:---:|:---:|:---:|:---:|
| repo_name | 检测仓库名称 | false | ${{github.repository}} |


| 输出参数| 描述| 示例|
|:---:|:---:|:---:|
| isFail | 检查是否失败 | true |

PS: action生成comment.txt文件，便于评论:
```
- 检测到敏感词export变动
<details>
<summary>详情</summary>

    {
    "export": {
        "debian/test": {
            "b": [
                "export1236"
            ]
        }
    }
}
</details>
```