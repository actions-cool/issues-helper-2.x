---
toc: menu
---

## ð `token` è¯´æ

éæ¥æ push æéçäººå tokenã

- [ä¸ªäºº token ç³è¯·](https://github.com/settings/tokens)
  - éå¾é `Full control of private repositories`
- é¡¹ç®æ·»å  secrets
  - éæ© settingsï¼éæ© secretsï¼éæ© `New repository secret`
  - `Name` ä¸ actions ä¸­ä¿æä¸è´
  - `Value` å¡«ååæä¸ªäººç³è¯·ç token

å½ actions ä¸å¡«å token æ¶ï¼æè¾å¥ `${{ secrets.GITHUB_TOKEN }}`ï¼ä¼é»è®¤ä¸º `github-actions-bot`ã[æ´å¤æ¥ç](https://docs.github.com/en/free-pro-team@latest/actions/reference/authentication-in-a-workflow)ã

## ð GitHub ç¸å³ææ¡£

- [GitHub Actions è¯­æ³](https://docs.github.com/en/free-pro-team@latest/actions/reference/workflow-syntax-for-github-actions#on)
- [å·¥ä½æµè§¦åæºå¶](https://docs.github.com/en/free-pro-team@latest/actions/reference/events-that-trigger-workflows)

## ð `outputs` ä½¿ç¨

```yml
- name: Create issue
  uses: actions-cool/issues-helper@v1
  id: createissue
  with:
    actions: 'create-issue'
    token: ${{ secrets.GITHUB_TOKEN }}
- name: Check outputs
  run: echo "Outputs issue_number is ${{ steps.createissue.outputs.issue-number }}"
```

æ´å¤æ¥çï¼

1. https://docs.github.com/en/free-pro-team@latest/actions/creating-actions/metadata-syntax-for-github-actions#outputs
2. https://docs.github.com/en/actions/reference/workflow-syntax-for-github-actions#jobsjob_idoutputs

## ð `includes` æ ¡éªè§å

```js
"title-includes": 'x1,x2'

x1
x2

"x1y3y2"  true
"y2 x1"   true
"x2"      true
"x3"      false
```

```js
"title-includes": 'x1,x2/y1,y2'

x1 + y1
x2 + y1
x1 + y2
x2 + y2

"x1y3y2"  true
"y2 x1"   true
"1x2y"    false
"x1"      false
```

## ð `Reactions` ç±»å

| content | emoji |
| -- | -- |
| `+1` | ð |
| `-1` | ð |
| `laugh` | ð |
| `confused` | ð |
| `heart` | â¤ï¸ |
| `hooray` | ð |
| `rocket` | ð |
| `eyes` | ð |

å¦éè¯¦ç»äºè§£ï¼å¯ [æ¥ç](https://docs.github.com/en/free-pro-team@latest/rest/reference/reactions)ã

## ð `comment-id`

ç¹å»æä¸ªè¯è®ºå³ä¸è§ `Â·Â·Â·` å¾æ ï¼éæ© `Copy link`ï¼url æ«å°¾æ°å­å³æ¯ `comment_id`ã
