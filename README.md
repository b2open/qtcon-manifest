# qtcon-manifest
=================

Primeiro é necessario instalar a ferramenta repo do Google, execute as rotinas:

      $ mkdir ~/bin
      $ PATH=~/bin:$PATH

      $ curl http://commondatastorage.googleapis.com/git-repo-downloads/repo > ~/bin/repo
      $ chmod a+x ~/bin/repo

Agora iremos criar um diretorio e realizar o repo para o nosso repositorio do manifesto:

      $ mkdir ~/rpi-yocto
      $ cd ~/rpi-yocto
      $ repo init -u https://github.com/b2open/qtcon-manifest -b qtcon2020


Para realizar pull down do metada dos repositorios execute:

      $ repo sync

Para configurar o ambiente e iniciar o build da image:

      $ cd ~/rpi-yocto
      $ source setup-environment
      $ bitbake qtcon-image-eglfs


# OBS: É mandatorio possuir pelo menos 50G de espaço em disco disponivel
