### 分支命名规范：

1. **功能点开发分支（Feature Branch）**:
   - 命名规范：`feature/<模块或功能点>`
   
2. **错误修复分支（Bugfix Branch）**:
   - 命名规范：`bugfix/<错误编号或简短描述>
   
3. **发布分支（Release Branch）**:
   - 命名规范：`release/<版本号>
   
4. **紧急修复分支（Hotfix Branch）**:
   - 命名规范：`hotfix/<错误编号或简短描述>
   
5. **主分支（Master Branch）**:
   - 命名规范：通常就是 `master`，不过有些项目可能会使用 `main` 作为主分支的名称。

### 从开发到版本发布的流程：

1. **创建功能点开发分支**:
   - 从 `dev` 分支检出新的功能分支：`git checkout -b feature/1.0.0-module-feature`

2. **开发功能**:
   - 在功能分支上进行开发，添加新功能。

3. **提交更改**:
   - 将更改提交到本地分支：`git commit -m "Add new feature"`

4. **推送到远程仓库**:
   - 将本地分支推送到远程仓库：`git push -u origin feature/1.0.0-module-feature`

5. **功能开发完成**:
   - 开发和测试完成后，将功能分支合并回 `dev` 分支:`git merge feature/1.0.0-module-feature`  

6. **创建发布分支**:
   - 从 `dev` 分支检出发布分支，例如：`git checkout -b release/1.0.0`

7. **准备发布**:
   - 在发布分支上进行最后的测试和准备，如文档更新、版本号更新等。

8. **合并发布分支到主分支**:
   - 将发布分支合并回 `master` 分支，例如：`git merge release/1.0.0`

9. **标记版本**:
   - 使用标签标记发布点，例如：`git tag -a v1.0.0 -m "Version 1.0.0 release"`

10. **推送标签到远程仓库**:
    - 将标签推送到远程仓库，例如：`git push origin v1.0.0`

11. **发布到生产环境**:
    - 将 `master` 分支的代码部署到生产环境。

12. **合并发布分支到开发分支**:
    - 将发布分支的更改合并回 `dev` 分支，以准备下一次迭代。

13. **删除临时分支**:
    - 删除不再需要的本地和远程分支，例如：`git branch -d release/1.0.0` 和 `git push origin --delete release/1.0.0`

