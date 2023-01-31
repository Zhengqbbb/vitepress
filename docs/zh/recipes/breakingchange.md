# markBreakingChangeMode

> 添加 ! 标识，表明该 commit 消息属于重大变更

See: 该规则来自 [Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0/#examples)<br>
E.g:
```text
# Commit message 带有 ! 提示重大变更
feat!: send an email to the customer when a product is shipped

# Commit message 与范围以及 ! 标识提示重大变更
feat(api)!: send an email to the customer when a product is shipped

# Commit message 带有 ! 提示重大变更以及底部说明
chore!: drop support for Node 6

BREAKING CHANGE: use JavaScript features not available in Node 6.
```

## 使用配置项: `markBreakingChangeMode`
> 额外添加 "BREAKINGCHANGE"的提问，询问是否需要添加 =="!"== 标识

```js{6}
// .commitlintrc.js

/** @type {import('cz-git').UserConfig} */
module.exports = {
  prompt: {
    markBreakingChangeMode: true
  }
};
```

示例:
![demo-gif](https://user-images.githubusercontent.com/40693636/175775159-710b69c6-ab55-4957-9195-6f963d95ba2e.gif) <!-- size=688x263 -->

## 使用 commitizen CLI + cz-git
可以尝试运行命令自动添加标识:
```sh
break=1 cz
```
示例:
![demo-gif](https://user-images.githubusercontent.com/40693636/174949733-d5cd7f0d-ac81-40e8-8cb9-158737330d7a.gif) <!-- size=688x265 -->

## 使用 cz-git CLI `czg`
可以尝试运行命令自动添加标识:
```sh
czg break
```
示例:
![demo-gif](https://user-images.githubusercontent.com/40693636/175755362-2fdeed9e-cf05-4f41-b317-453154a5775c.gif) <!-- size=688x248 -->
