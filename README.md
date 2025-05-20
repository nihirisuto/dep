```
mkdir base && cd base
git clone --depth 1 https://github.com/nihirisuto/dep.git \
	&& cd dep/dep \
	&& for i in {0..3}; do (echo "working > assets$i.pk3..." \
	&& cat dep${i}_* > ../../assets${i}.pk3 &); done; wait \
	&& cd ../.. && rm -rf dep && echo "asset files created in $pwd"
```