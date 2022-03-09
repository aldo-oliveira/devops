# Linux Comandos

**Trabalhando com Diretórios e Arquivos:**

pwd - Diretório corrente completo
ls - Listar Arquivos
echo - exibir mensagens na tela
cat <file> - exibir conteudo de um arquivo na tela
clear - limpa tela
whoami - nome do usuario que esta sendo usado
cd <dir>- entrar em um diretório
mkdir <dir>- criar diretório
rmdir <dir>- excluir diretorio
rm <file> - excluir um arquivo

rm -rf <pasta> apaga toda pasta e arquivos
cp <file> <newfile> - copiar/duplicar um arquivo
mv <file> <newfile> - renomear arquivos
touch <file> - altera a data para a atual
help - lista geral de codigos
date - data atual
head <file>

df -h - mostra espaço em disco

**coringas:**

-r (recursivo) ex: cp -r <dir> <newdir> duplica a estrutura
? - oculta caracteres ex: cat arquivo?.txt
* - oculta todos os caracteres seguintes ex: cat arquiv*.txt

**compactação:**

zip <file.zip> <dir> - compacta no diretorio informado
zip -r <file.zip> <dir> - -r (recursivo) inclui subdir
unzip -l <file.zip> lista os arquivos do arquivo zip
unzip -q <file.zip> - -q (quiet) modo silencioso
tar -cz <dir> > file.tar.gz - -c = create / z = zip
tar -xz < work.tar.gz -xz=extract zip, simbolo '<' entrada de dados
tar -cjf work.tar.bz2 <dir>

**vi:**

i = entra no modo edição
ESC = volta no modo navegação
w + Enter = salvar alguma modificação
q! + Enter = sair sem salvar
q + Enter = sair
setas: para navegação
i: inclui (na posição atual)
a: adiciona (na posição posterior)
Shift+A: adiciona (fim da linha)
x: remove caracteres (*n* x remove *n* caracteres)
dd: remove uma linha (*n* dd remove *n* linhas)
y = copia a linha
p = cola a linha

**outros:**

dpkg —list (listar todos os programas instalados)

sudo find . -print | grep -i <palavra> (buscar arquivos ou diretorios em subdiretorios)
