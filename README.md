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