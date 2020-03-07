# Ubuntu18 Singularity

Ubuntu Linux 18.04 (Bionic) のSingularityコンテナ


## 前提

Ubuntu Linuxにdebootstrap他の必要なソフトをインストールする場合は以下の通り。

    sudo apt update
    sudo apt upgrade
    sudo apt install build-essential libtool automake libarchive-dev debootstrap git

Singularityはversion 2.x系でも3.x系でもよい。（今はもう3.x系推奨）

- [Singularityのインストール方法（Official Document)](https://sylabs.io/guides/3.5/admin-guide/installation.html) 



## 使い方

    # コンテナのビルド
    git clone http://gitlab.ddbj.nig.ac.jp/oogasawa/singularity-ubuntu18
    cd singularity-ubuntu18
    mkdir $HOME/singularity-images
    sudo singularity build --sandbox $HOME/singularity-images/ubuntu18 Singularity
    
    # コンテナ内での作業
    sudo singularity shell --write $HOME/singularity-images/ubuntu18
    
    # *.sifファイルに固めてスパコンなど共用計算機にコピー
    sudo singularity build ubuntu18.sif $HOME/singularity-images/ubuntu18
