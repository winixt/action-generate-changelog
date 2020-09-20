# action-generate-changelog

自动生成 changelog，并生成 github release draft。

使用前先执行：

```bash
echo '# Change Log\n\n<!-- DO NOT CHANGE THESE COMMENTS -->\n<!-- insert-new-changelog-here -->' > CHANGELOG.md
```

项目package.json里面添加 changelog 配置:

```
  "changelog": {
    "bugsUrl": "https://redmine.example.com/issues/",
    "authorName": true,
    "authorEmail": false,
    "settings": {
      "feat": {
        "title": ":rocket: New Feature",
        "enable": true
      },
      "fix": {
        "title": ":bug: Bug Fix"
      },
      "perf": {
        "title": ":running_woman: Performance"
      },
      "revert": {
        "title": ":leftwards_arrow_with_hook: Revert"
      },
      "refactor": {
        "title": "♻ 代码重构"
      },
      "docs": {
        "title": ":memo: Documentation",
        "enable": true
      },
      "style": {
        "title": ":eyeglasses: Spec Compliance",
        "enable": true
      },
      "test": {
        "title": "✅ 测试",
        "enable": false
      },
      "build": {
        "title": "👷‍ 构建",
        "enable": false
      },
      "ci": {
        "title": "🔧 CI 配置",
        "enable": false
      },
      "chore": {
        "title": "🎫 其他更新",
        "enable": false
      }
    }
  }
```
