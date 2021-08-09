## git push 에러 처리

```log
error: src refspec master does not match any
error: failed to push some refs to 'https://github.com/homkim......'
```

```sh
git init
git add .
git commit -m "message"
```

## 이름 이메일 넣어라고 나오는 경우

```sh
git config user.name "name"
git config user.email "email@example.com"
git remote add orgin "github.com/homkim/<repo_name>"
git push -u origin master
```

## git pull

```sh
git pull <url> master
```
