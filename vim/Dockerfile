FROM alpine
RUN apk add vim fish git curl tmux nodejs npm
RUN curl -flo ~/.vim/autoload/plug.vim --create-dirs \
				https://raw.githubusercontent.com/junegunn/vim-plug/master/plug.vim
RUN git clone https://github.com/lpmg11/configs.git 
RUN cp -r configs/vim/.vim ~
RUN cp configs/vim/vimrc ~/.vimrc
RUN vim -c "PlugInstall|q|q"
RUN fish -c "alias v='vim .' ; funcsave v"
WORKDIR /app/
