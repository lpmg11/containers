FROM alpine
RUN apk add vim fish git curl tmux nodejs npm
RUN git clone https://github.com/lpmg11/configs.git 
RUN curl -flo ~/.vim/autoload/plug.vim --create-dirs \
				https://raw.githubusercontent.com/junegunn/vim-plug/master/plug.vim
RUN cp -r configs/vim/.vim ~
RUN cp configs/vim/vimrctmp ~/.vimrc
RUN vim -c "PlugInstall|q|q"
RUN fish -c "alias v='vim .' ; funcsave v"
RUN cp configs/vim/vimrc ~/.vimrc
WORKDIR /app/
COPY ./src ./
