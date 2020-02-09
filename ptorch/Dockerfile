FROM nvidia/cuda:10.1-base-ubuntu18.04

RUN apt-get update && \
    apt-get install vim -y && \
    apt-get install python3-pip -y && \
    apt-get install git -y && \
    git clone https://github.com/preservim/nerdtree.git ~/.vim/pack/vendor/start/nerdtree && \
    vim -u NONE -c "helptags ~/.vim/pack/vendor/start/nerdtree/doc" -c q

COPY ./vimrc /root/.vimrc

RUN pip3 install torch torchvision pandas numpy matplotlib seaborn tqdm Pillow scikit-learn tensorflow tensorboard
