# Maiapkg - Gerenciador de Pacotes 

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

   [ --ajuda | -h ]

       Aparece o menu de ajuda.  

  
   [ --empacota | -b ] 

       Cria um pacote .$extensao . Precisa estar dentro do diretório
       principal do pacote para ser gerado. O mesmo será criado um
       diretório acima.
       Formato:  nome-versão-build.${extensao}

       Exemplo: maiapkg --empacota nome-versão-build.${extensao}  


   [ --instala | -i ]

       Instala o pacote .mpkg no seu sistema e criar um rastreador 
       no diretório /var/log/pacotes.

       Exemplo: maiapkg --instala nome-versão-build.${extensao}  


   [ --set-desc ]

       Gera uma descrição para o programa. 
       Obs: Tem que estar dentro da pasta do programa
       para gerar uma descrição. O arquivo gerado ficará 
       dentro da pasta ./desc/info.
      
       Exemplo: maiapkg --set-desc      
   
    
   [ --get-desc ]

       Mostra a descrição do pacote. A descrição mostrada estará 
       sendo verificado dentro da pasta ./desc/info em /tmp. 
       
       Exemplo: maiapkg --get-desc nome-versão-build.${extensao}  


   [ --remove | -r ]

       Remove arquivos, atalhos e pastas dos programas empacotados 
       e instalados com o maiapkg. 
       Ele consegue rastrear e ler o mapeamento do pacote em um arquivo 
       de rastreio dentro de /var/log/pacotes/

       Exemplo: maiapkg --remove nome_do_pacote  
 

   [ --verbose | -v ]

       Mostra os processos da instalação, detalhando arquivos e diretórios do programa.

      
 AUTOR  : Luiz Eduardo    CONTATO: distromaialinux@gmail.com 
