## Topic 3: Manipulating Content With Shell Commands

## cat
Displays the contents of a file on standard output(screen).

*$cat "file"*

## more 

Display the contents of a file on standard output(screen), displaying one screen at a time (ideal for large files)

*$more "file"*


## less

Display the contents of a file on standard output(screen), with pagination options

*$less "file"*

## head
Displays in the standard output (screen), the first ten line of the file per standard, and this value can be specified

*$head "file"*

## tail
Display in the standard output (screen), the last ten lines of the file per standard, and this value can be specified

*$tail "file"*

*$tail -f "file"* Displays in real time changes, ideal for monitoring hackers attacks 

# Part 2

### grep 

Search files or your standard entry for a character string

$grep <options> [string_or_regex] [file os path]

 * Ex: grep“root”  /etc/passwd
 * Ex.: cat/etc/passwd|  grep“root”
 * ls-l  /lib|  grep^d
 * ls-l  /lib|  grep-v  ^d
 * grep-r  root  /etc
 * grep-r  root  /etc|  more
 * grep-r  root  /etc|  less
 * ls-l  /etc|  grep2010
 * ls-l  /etc|  grep-v  ^d  |  grep2010

### egrep

Similar to grep -E using regex. 

### zgrep

Similar to grep using to search in zip files.

### wc
	
The command realize the count of lines, words or characters in a file or standard entry

* ls-l  /etc|  wc-l
* cat/etc/passwd|  wc-l
* wc-l  /etc/passwd
* ls-l  /etc|  grep^d  |  wc-l

### tr

translate or delete characters to standard input and display the result output 

$cat /etc/passwd | tr : ; 


### sed

filter and transform the text

$sed '/s/nologin/false' /etc/passwd

### diff

compare two files and shows the differences.

$ diff [file1] [file2]

### sort

alphabetically order a specific file or standard entry

$cat/etc/passwd|sort

$sort/etc/passwd

$cat/etc/passwd|  grep“/bin/bash”  |  cut-d  ‘:’  -f  1  |  sort  

 $  sort/etc/passwd|  grep“/bin/bash”  |  cut-d  ‘:’  -f  1  

### cut
Remove sections from each line of files

$ cut-d:  -f  1  /etc/passwd

### awk 

Similar to cut with more features

$awk-F:  ‘{ print$1 }’  /etc/passwd

$ls-lh/var/log/  |  awk-F “ ”  ‘{ print“Nome do arquivo: ” $9 “ -Tamanho: ” $5 }’

### zip
permit compress files in format zip

$zip -r dados.zip /etc

### unzip

permit decompress files in format zip or list your content 

$unzip dados.zip

$unzip dados.zip -d "/root/bak-etc"

### tar
 
Tar is an archiving program designed to store multiple files in a single file.

Packs data into a file without actually compressing.

compress / decompress files using the pattern gzip

$tar < options > [file] < options || path to compress 

* c -> Compress or packed data into a new file.
* x -> extract the content of a compressed file
* t -> list the content of a compressed file
* v -> display on screen what is being compressed or decompress
* p -> Preserves the permissions of the file
* r -> add files into package tar
* z -> Operation mode with the gzip compactor
* Z -> Operation mode with the compress compactor
* j -> Operation mode with the bzip2 compactor
* f -> Operation mode with file (the default is tape devices)

$tarczfarquivo.tar.gz  /etc/

$tarcjfarquivo.tar.bz2  /etc/

$tarcfempacotado.tar  /etc/

$tarxzfarquivo.tar.gz

$tarxzfarquivo.tar.gz  -C  /diretorio/destino/desejado/
