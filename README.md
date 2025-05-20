```shell
mkdir -p base && cd base
```

```shell
git clone --depth 1 https://github.com/nihirisuto/dep.git \
  && for i in {0..3}; \
       do echo " *** assets${i}.pk3..."; \
       find dep -name "dep${i}_*" -type f | sort | xargs cat > assets${i}.pk3; \
     done \
  && rm -rf dep && echo " *** asset files created in $(pwd)"
```