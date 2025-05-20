```
git clone --depth 1 https://github.com/nihirisuto/dep.git \
	&& cd dep && mkdir -p assembled \
	&& for i in {0..3}; do (echo "working > $i.pk3..." \
	&& cat dep${i}_* > assembled/assets${i}.pk3 &); done; wait
```