# Maiapkg 
## Gerenciador de pacotes para usar com Linux From Scratch 

# AUTOR : Luiz Eduardo - distromaialinux@gmail.com

VERSÃO : 1.0

DESCRIÇÃO :
  Maiapkg é um gerenciador de baixo nível 
  feito para minha distribuição Maialinux.    
  Changelog :
  ( Versão 1.0 )
  - Adicionado verificação de dados.
  - Suporte a informações do pacote.
  - Diretório desc contendo informações do pacote
  - Adicionado as seguintes opções de comandos:
  ( --ajuda, --empacota, --instala, --set-desc, --get-desc, --remove, --verbose ) 

### Para aparecer o menu de ajuda 

### Comando [ --ajuda | -h ]:
	maiapkg --ajuda

### Para criar um pacote você precisa estar dentro do diretório principal do pacote para ser gerado. O mesmo será criado um diretório acima. Formato:  nome-versão-build.${extensao}
### Exemplo: maiapkg --empacota nome-versão-build.mpkg   

### Comando [ --empacota | -b ]:
 	maiapkg --empacota 

### Para instalar o pacote .mpkg no seu sistema e criar um rastreador no diretório /var/log/pacotes.
### Exemplo: maiapkg --instala nome-versão-build.mpkg    

### Comando [ --instala | -i ]:
	maiapkg --instala
       
### Para gerar uma descrição para o programa, você tem que estar dentro da pasta do programa. 
### O arquivo gerado ficará dentro da pasta ./desc/info. 

### Comando [ --set-desc ]:
	 maiapkg --set-desc 
       
### Para mostrar a descrição do pacote use o parametro --get-desc. A descrição mostrada estará sendo verificado dentro da pasta ./desc/info em /tmp. 
### Exemplo: maiapkg --get-desc nome-versão-build.mpkg   

### Comando [ --get-desc ]:
	maiapkg --get-desc
      

  

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
