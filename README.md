# OCP 佈署nuxt專案設定

# Installation

> We recommend you use npm

1. docker build

```shell
cd package
docker build -t my-nuxt-app .
docker run -d -p 3000:3000 my-nuxt-app
```

2. OCP

```shell
oc new-build --name=my-nuxt-app --binary --strategy=docker
oc start-build my-nuxt-app --from-dir=. --follow
oc new-app my-nuxt-app
oc expose svc/my-nuxt-app
```