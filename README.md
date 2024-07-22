# Pre requirements
### Golang
```
brew install go
```

### Kubebulder

```
# download kubebuilder and install locally.
curl -L -o kubebuilder "https://go.kubebuilder.io/dl/latest/$(go env GOOS)/$(go env GOARCH)"
chmod +x kubebuilder && sudo mv kubebuilder /usr/local/bin/
```


# 구성 
```
kubebuilder init --domain ben.com --repo github.com/titaniper/tenant-operator
kubebuilder create api --group batch --version v1 --kind CronJob
```

# 문서 
- https://book.kubebuilder.io/architecture

# ㅌㅔ스트
https://book.kubebuilder.io/quick-start
```
make manifests

-- CRD 클러스터에 넣기
make install
-- 하하
make run

-- CRD 배포
kubectl apply -k config/samples/


devjyk/tenant-operator

make docker-build docker-push IMG=devjyk/tenant-operator
make deploy IMG=devjyk/tenant-operator
```

인터페이스 수정 후에
```
make build
```