# Atividade 3

1 –Descreva resumidamente a função dos comandos abaixo:

grep = realiza buscas por aquivos ou expressões contidas dentro de seu conteúdo 

wc = realiza a contagem de linhas, colunas, caracteres ou bytes dentro de um aquivo.
 
sort = organiza a saída em ordem alfabética.

cut =  realiza remoção de sessões dentro de um arquivo.

tar = realiza o arquivamento de vários aquivos em um com compressão ou não. 

2 –Qual o comando para listar em ordem alfabética o conteúdo do arquivo “/etc/group”?

$ sort /etc/group

3 –Utilizando o comando da questão anterior, concatene um novo comando (na mesma linha)que realiza a contagem da quantidade de linhas do conteúdo gerado pelo primeiro comando.

$ sort /etc/group | wc -l

4 – Através do comando “cut", filtre a saída do comando “ls  -l  /”, de forma que seja exibido apenas as permissões, data e nome dos diretórios listados.

$ls -l / | tr -s ' ' | cut -d ' ' -f 1,6,7,8,9 | grep \^d

5 – Modifique a linha de comando da questão anterior de forma que sejam exibidas apenas as permissões, usuário e grupo proprietários de cada diretório, e o nome do diretório.

$ls -l / | tr -s ' ' | cut -d ' ' -f 1,3,4,9 | grep ^d
 
6–Através do comando “grep”, filtre a saída do comando “ls-l /proc”, exibindo os arquivos/diretórios que não possuem o usuário e grupo“root” como proprietário.

$ls -l /proc | grep -v 'root' 

7–Acesse o seu diretório pessoal e compacte apenas o conteúdo do seu diretório pessoal para um arquivo chamado ”seu_nome.tar.gz” (o arquivo “seu_nome.tar.gz” deverá ficar no diretório pessoal. Ex.: “/root/guilherme.tar.gz”).

$ tar czfv michel.tar.gz /home/michel/

8–Liste o conteúdo do arquivo “seu_nome.tar.gz” e o conteúdo do seu diretóriopessoal e verifiquese ambos mostram a mesma quantidade de arquivos.

$ tar tf michel.tar.gz

9–Compacte o diretório "/etc" e todo o seu conteúdo em um novo arquivo de nome "backup-etc.tar.xxx" com os compactadores GZIP e BZIP2 (onde "xxx" será alterado de acordo com o compactador utilizado):

Comando para compactar com o GZIP = 

$tar czfv backup-etc.tar.gzip

Comando para compactar com o BZIP2 = 

$tar cjfv backup-etc.tar.bzip2

 
10–Copie os arquivos gerados para o diretório pessoal do usuário "root".

$cp backup-etc.tar.* /root


11–Execute o comando "ls-lh/root", onde será possível visualizar o tamanho de cada um dos arquivos gerados na questão 9.Observe qual comando realizou uma compressão mais eficiente.

Foi observado que o bzip2 apresentou uma melhor compactação para este caso.

12 –Crie um diretório com o nome “restore-gzip/” dentro do seu diretório pessoal e descompacte o conteúdo do arquivo “tar” compactado com o compactador GZIPna questão 9 dentro deste diretório(/root/restore-gzip/).

$mkdir restore-gzip

$tar xzfv backup-etc.tar.gzip -C /root/restore-gzip

13 –Crie um diretório com o nome “restore-bzip/” dentro do seu diretório pessoal e descompacte o conteúdo do arquivo “tar” compactado com o compactador BZIP2na questão 9 dentro deste diretório (/root/restore-bzip/).

$mkdir restore-bzip

$tar xjfv backup-etc.tar.bzip -C restore-bzip