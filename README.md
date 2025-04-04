# Maiapkg 
## Gerenciador de pacotes para usar com Linux From Scratch 

# AUTOR : Luiz Eduardo - distromaialinux@gmail.com

VERSÃO : 0.1

DESCRIÇÃO :
  Maiapkg é um gerenciador de baixo nível 
  feito para minha distribuição Maialinux.    
  Changelog :
  ( Versão 0.1 )
  - Adicionado verificação de dados.
  - Suporte a informações do pacote.
  - Diretório desc contendo informações do pacote
  - Adicionado as seguintes opções de comandos:
  ( --help, --build, --install, --set-info, --show-info, --remove, --verbose ) 

### Para aparecer o menu de ajuda 

### Comando [ --help | -h ]:
	maiapkg --help

### Para criar um pacote você precisa estar dentro do diretório principal do pacote para ser gerado. O mesmo será criado um diretório acima. Formato:  nome-versão-build.${extensao}
### Exemplo: maiapkg --empacota nome-versão-build.mpkg   

### Comando [ --build | -b ]:
 	maiapkg --build 

### Para instalar o pacote .mpkg no seu sistema e criar um rastreador no diretório /var/log/pacotes.
### Exemplo: maiapkg --install nome-versão-build.mpkg    

### Comando [ --install | -i ]:
	maiapkg --install
       
### Para gerar uma descrição para o programa, você tem que estar dentro da pasta do programa. 
### O arquivo gerado ficará dentro da pasta ./info/info. 

### Comando [ --set-info ]:
	 maiapkg --set-info 
       
### Para mostrar a descrição do pacote use o parametro --show-info. A descrição mostrada estará sendo verificado dentro da pasta ./info/info em /tmp. 
### Exemplo: maiapkg --show-info nome-versão-build.mpkg   

### Comando [ --show-info ]:
	maiapkg --show-info
      


### Para remover os pacotes .mpkg, use o parâmetro --remove ou -r. 
### Ele consegue rastrear e ler o mapeamento do pacote em um arquivo de rastreio dentro de /var/log/pacotes/
### Exemplo: maiapkg --remove nome_do_pacote  

### Comando [ --remove | -r ]:
	maiapkg --remove

### Para mostrar os processos da instalação, detalhando arquivos e diretórios do programa, use o parâmetro --verbose ou -v.
### Exemplo: maiapkg -v -i nome_do_pacote.mpkg  

### Comando [ --verbose | -v ]:
	maiapkg --verbose
       

## Modo de instalar:

### Baixe o arquivo Maiapkg:
	git clone https://github.com/Maialinux/Maiapkg.git

### Entre na pasta Maiapkg/
	cd Maiapkg/

### Descompacte o arquivo:
	tar -xvf Maiapkg-main.tar.gz

### Dê permissão de executável:
	chmod 755 ./Maiapkg/maiapkg

### Copie o arquivo maiapkg para o seguinte diretório /usr/sbin:
	cp -v ./Maiapkg/maiapkg /usr/sbin/

### Teste com o seguinte comando:
	maiapkg -h


### AUTOR  : Luiz Eduardo    CONTATO: distromaialinux@gmail.com 

### Observação:
Este gerenciador de pacotes que eu fiz, foi baseado no curso do slackjeff.

### Github:
https://github.com/slackjeff. 

### Canal do Youtube do Slackjeff:
Canal no youtube: https://www.youtube.com/@SlackJeff
