# Ubuntu18 Singularity

Ubuntu Linux 18.04 (Bionic) のSingularityコンテナ


## 前提

- Singularityがインストールされていること。
    - [Singularityのインストール方法（Official Document)](https://www.sylabs.io/guides/2.6/user-guide/installation.html) 
    

## 使い方

    # コンテナのビルド
    git clone http://gitlab.ddbj.nig.ac.jp/oogasawa/ubuntu18-singularity
    sudo singularity build --sandbox your-container-name ubuntu18-singularity/ubuntu18.txt
    
    # コンテナ内での作業
    sudo singularity shell --write your-container-name
    
