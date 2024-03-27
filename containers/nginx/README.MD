### 💡 情境

透過 Dockerfile 將網頁設定好，並打包成 image 後，部屬到自己的 docker registry 上

---

1. 將 dockerfile 以 tag 方式打包
```
docker build -t localhost:5000/nginx-test .
```

2. 確認是否已登入 docker registry

3. 推到 docker registry 上
```
docker push localhost:5000/nginx-test
```

### 📦 拉下來試試看
```
docker run -p 7777:80 --name nginx-test-123 localhost:5000/nginx-test
```