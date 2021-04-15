# Atividade4 –Comandos Shell
 

1 –Descreva resumidamente a função dos comandos abaixo:

du =  Mostra informações sobre o tamanho de arquivos e diretórios. 

df = Mostra informações sobre o espaço livre dos discos. 

free = Mostra informações sobre o uso de memoria e do SWAP 

uptime = mostra informações de de quanto tempo o sistema esta no ar

dmesg = Mostra todo Hardware carregado no sistema 

2–Qual a linha de comando que retorna resumidamente a quantidade em megabytes que o diretório “/lib”está ocupando no sistema?RESPOSTA (Qual o tamanho do diretório “/lib”) =

$ du -hs /lib 

3 –Qual a linha de comando que retorna informações sobre a utilização do disco? (espaço utilizado e espaço livre de cada partição). Executeo comando e responda qual a quantidade de espaço disponível em disco.RESPOSTA (qual a quantidade de disco disponível?) = 

4 –Verifique em sua máquina virtual Linux, a quantidade de memória disponível no sistema. RESPOSTA (qual a quantidade de memória disponível?) = 

$ free -h

livre 114M
Cache 2,0G
Disponível 1,8G



5 –Através da utilização dos comandos “dmesg” e “grep” concatenados, verifique o caminho que podemos acessar o drive de CD-ROM (caminho do dispositivo/device).RESPOSTA (qual ocaminho para acessar o dispositivo de CD-ROM?) = 

dmesg | grep CD-ROM

6 –Através do comando “ifconfig”ou “ip address”, identifique a interface Ethernet disponível em seu sistema e atribua um endereço IP.

enp0s10

$ ip address add 192.168.0.123/24 dev enp0s10

7 –Através do comando “ping” realize um teste de conectividade com um site. Ex.: www.google.com. OBS.: Provavelmente será mais viável executar um “dhclient”com o Virtual Box no modo “NAT”ou “Bridge”.PARTE 2 -GERENCIADORES DE BOOT E INICIALIZAÇÃO DO SISTEMAOBS.: Este conteúdo não foi abordado nos vídeos do curso, por não se tratar de um tópico prático, além do fato de possuir um peso menor no exame de certificação e no dia-a-dia com o GNU/Linux. Entretanto, coloquei aqui por ser importante sabermos que existe e para que serve. Em caso de dúvidas, envie uma mensagem pela plataforma.

$ ping www.google.com

8–Faça uma pesquisa e descreva pelo menos duas diferenças entre os gerenciadores de Boot“LILO” e “GRUB”.

O LILO não possui interface de comando interativa enquanto o GRUB possui.

O LILO não suporta inicialização a partir de uma rede, enquanto o GRUB suporta.

O LILO armazena informações sobre a localização dos sistemas operacionais para carregar fisicamente no MBR. Se você altear seu arquivo de configuração do LILO, precisará reescrever o carregador de inicialização do estágio um do LILO no MBR. Coparado com o GRUB, essa é uma opção muito mais arriscada, pois um MBR mal configurado pode deixar o sistema não inicializável. Com o GRUB, se o arquivo de configuração estiver configurado incorretamente, ele simplesmente assumirá o padrão da interface de comandos do GRUB 

O LILO carrega apenas Linux e outros gerenciadores de inicialização. E o GRUB carrega um grande número de sistemas operacionais

O LILO trabalha carregando-se em um espaço que caiba no MBR. O GRUB tem dois estágios, carrega o estágio 1 do MBR e o estágio 2 do /boot, junto com sua configuração.  

9–Em relação ao sistema GNU/Linux, o que significa “runlevel”?

RESPOSTA = O runlevel é um nível de execução do sistema operacional.

10–Sabemos que existem 7 “runlevels”. Explique a função/finalidade de cada um deles:

RUNLEVEL  0 = Este é o nível de execução halt. Sendo assim se você chamar este runlevel, o equipamento vai desligar.
 
RUNLEVEL  1 = Este é o modo de execução mono usuário. (modo de recuperação)
  
RUNLEVEL  2 = Não é utilizado. Usuário poderá personalizar como quiser.
  
RUNLEVEL  3 = Este é o nível de execução multi-usuário sem interface gráfica.

RUNLEVEL  4 = Não é utilizado. Usuário poderá personalizar como quiser.

RUNLEVEL  5 = Geralmente o nível de execução padrão. Modo multi-usuário com interface gráfica(GUI).

RUNLEVEL  6 = Modo de reboot. Logo, se você chamar este runlevel, o equipamento vai reiniciar.   
