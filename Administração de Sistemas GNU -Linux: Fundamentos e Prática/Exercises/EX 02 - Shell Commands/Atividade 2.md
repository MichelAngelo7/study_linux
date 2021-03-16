# Atividade 02
 1 – Execute o comando a seguir e descreva o resultado:mkdir-p {teste,docs/{listas,rh,pub},slides/{Linux,Windows}}
 
 
 RESPOSTA =  Cria 3 diretórios teste, docs e slides, sendo que dentro do diretório docs existem 3 subdiretórios listas, rh, pub. No diretório Slides encontramos 2 subdiretórios Linux e Windows.
 
 2 – Utilizando o mesmo contexto/sintaxe da questão 1, crie a seguinte estrutura de diretóriosno Linuxcom apenas um comando:
 
 RESPOSTA = mkdir -p Udemy/{Linux/{Atividades,Slides},Redes/{Atividades,Slides},Servidores/{Atividades,Slides}}
 
 3 – O que significa o parâmetro “-r” no comando “cp”? Porque é uma boa pratica usá-lo?
 
 RESPOSTA = 
 
 O  parâmetro -r copia os arquivos e diretórios de forma recursiva não deixando de lado os arquivos e diretórios presentes dentro dos subsdiretorios 
 
 4 –Crie a seguinte estrutura de diretórios dentro do seu diretório pessoal:
 
 ~/atividade/sistema/linux/
 
 mkdir -p  ~/atividade/sistema/linux/
 
 
 
  
 5 –Encontre os arquivos listados abaixo dentro de algum diretório do sistema Linux e copie-os para dentro do seu diretório ~/atividade/sistema/
 
 * fstab
 * resolv.conf 
 * passwd 
 * shadow   
 * group
 * inittab 
 
 $ cp -rp /etc/{fstab,resolv.conf,passwd,shadown,group,inittab} ~/atividade/sistema
 
 6 – Altere a estrutura de diretórios da questão 04 para a seguinte: ~/atividade/pratica/sistema/operacional/linux
 
 $mkdir ~/atividades/pratica
 $mv ~/atividades/sistema ~/atividades/pratica
 $mkdir ~/atividades/pratica/sistema/operacional
 $mkdir ~/atividades/pratica/sistema/linux ~/atividades/pratica/sistema/operacional
 
 7 – Faça uma pesquisa na Internet e responda a finalidade de cada um dos arquivos listados na questão 05:
 
 * /etc/fstab --> O arquivo fstab pode ser usado para definir partições do disco, vários outros dispositivos de bloco ou sistemas de arquivo remotos que devem ser montados no sistema.
  
 * /etc/resolv.conf --> E um aquivo usado em vários sistemas operacionais para configuração do DNS do sistema.
 
 * /etc/passwd --> e um banco de dados de informações baseadas em texto sobre os usuários que podem logar no sistema ou outras identidades de usuário do sistema operacional que possuem processos em execução.    
 
 * /etc/shadow --> e usado para incrementar o nível de segurança das senhas ao restringir o acesso de todos os usuários, podem pode ser acessado por usuários privilegiados, normalmente os dados são salvos em arquivos de acesso apenas pelo superusuário.   
 
 * /etc/group --> e um arquivo que de sistema que define os grupos ao quais os usuários pertencem em sistemas UNIX, como o Linux e o BSD.
 
 * /etc/inittab --> Descreve processos que vão iniciar automaticamente junto com o sistema operacional.
 
8 –Apague o diretório de nome “operacional” e todo o seu conteúdo, criado na questão 06.

$rm -rf ~/atividades/pratica/sistema/operacional

9 –Altere o nome do diretório “pratica” criado na questão 06 para “teste”(mantendo a estrutura de subdiretórios existente).

$mv ~/atividade/pratica ~/atividades/teste

10 – Os comandos“cat”, “more” e “less” são comando de visualização de conteúdo. Quais as diferenças entre eles? 

* cat   --> Exibe o conteúdo do arquivo sem nem um tipo de paginação.
* more  --> Exibe o conteúdo do arquivo e ao final da dela aguarda que usuário pressione um botão para continuar a exibição ate finalizar todo conteúdo
* less  --> Exibe o conteúdo do arquivo com recursos de paginação ideal para arquivos extensos. 


11 –Vamos supor que você deseja executar um programa que levará muito tempo para ser executado e que sua saída é muito extensa. Como podemos redirecionar toda a saída deste comando para um arquivo com o nome “log.txt”? 
(OBS.: Vamos supor que o comando se chama “app.sh”).

$app.sh > log.txt


12 –No mesmo contexto da questão anterior, qual a linha de comando que deveria ser utilizada caso seja necessário separar as mensagens de erro das mensagens de sucesso?

(O erro deve ser armazenado em “erro.log” e as mensagens de “sucesso” em “ok.log”)

$app.sh 2> ~/erro.log > ~/ok.log


13 –(Concatenação) –Descreva qual a finalidade do comando a seguir:DICA: Execute este comando em sua VM, porém, em partes para comparar as diferenças de saída para cada um dos comandos executados (Ex.: primeiro o “cat /etc/passwd”, depois o “cat /etc/passwd | grep /bin/false”, e assim sucessivamente).OBS.: Caso a sua VM seja um CentOS, utilize "/bin/bash" ao invés de "/bin/false".


RESPOSTA = executa o comando cat para exibir o conteúdo arquivo passwd, o resultado e enviado para o comando grep que buscar pela expressão "/bin/false", o resultado e encaminhado para o comando cul exibe o conteúdo da linha apenas ate a primeira ocorrência de  ":".

14 –Cite um exemplo de concatenação de comandos e justifique a finalidade.(Realize um teste em sua VM a partir dos comandos que você já conhece e posteriormente, justifique a finalidade).


COMANDO 1 = &&

COMANDO 2 = ||

FINALIDADE 1 = executa o primeiro comando caso o a saída do comando seja executada com sucesso ele executa o segundo comando.

FINALIDADE 2 = executa o primeiro comando caso ocorra um erro ele executa o segundo comando.