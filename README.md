# Nuxt Crash Course

https://www.youtube.com/watch?v=Wdmi4k7sFzU


## 起動
```
docker run -itd --rm --name nuxt-crash-course -p 3333:3000 --workdir /app --mount "type=bind,source=$(pwd),target=/app" -e "NUXT_HOST=0.0.0.0" node:16-alpine sh -c "cd client && yarn dev"
```