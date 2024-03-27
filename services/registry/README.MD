### 💡 情境

透過 docker-compose 將 docker registry 啟動，並自行更改密碼。

此範例有將 registry 的密碼，以及上傳的 image 映射到 volume 中。

---

1. 透過 docker-compose 啟動 registry
```
docker-compose up
```

2. 進入容器
```
docker exec -it docker-registry /bin/sh
```

3. 新增 registry 的帳號密碼，因有將 htpasswd volume 出去，下完指令後，可以看看是否新增成功
```
apk add apache2-utils
htpasswd -B /auth/htpasswd accounttt
```

### 📦 本地 docker 登入
```
docker login localhost:5000
```