# ci-check-action
整合CI检查各个检查作为action使用，每个检查大类单独创建分支

# action列表
* api-check: API接口检查：检查PR中是否存在对外接口的删除和修改
* debian-check: Debian接口检查
  * debian-prefix-check: 检查PR中是否存在debian前缀的文件
  * debian-version-check: 检查PR中是否deian/changelog版本是否正确
  * debian-keys-check: 检查PR文件中是否存在指定敏感词设置
* static-check: 静态代码检查
  * golangci-lint: golangci-lint检查
  * cpp-check: cppcheck检查
  * shell-check: shellcheck检查
* post-check: 检查完成后添加评论和reviewer人员
* send-data: 检查完成后发送数据到明道云