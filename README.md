# Calendário.bat

![descrição](https://www.shutterstock.com/image-vector/december-2024-calendar-leaf-flat-600nw-2529607467.jpg)

# O que aprendi?
Na aula de hoje, exploramos e aprofundamos o uso dos arquivos de lote (.bat) no Windows. Aprendemos que os arquivos .bat são scripts que automatizam tarefas repetitivas por meio de comandos do Prompt de Comando (CMD).
Vimos como criar, editar e executar arquivos .bat, além de comandos essenciais como echo, cls, pause, shutdown, mkdir, entre outros. Também abordamos a lógica condicional com if e o uso de loops com for, permitindo maior controle sobre os scripts. No geral a aula foi bem produtiva e comunicativa, graças as intruções realizadas pelos instrutores conseguimos atingir um resultado excelente do que foi exposto.

# Descrição do script
O script sugerido tinha o papel de organizar um calendário contendo meses, dias e um ano. Primeiramente o introduz o comando @echo off impedindo que os comandos do script não sejam exibidos na tela durante a execução. Logo após ele verifica se o diretório passado como primeiro argumento (%1) existe. Se ele não existir, ele cria duas pastas. Depois ele calcula quantos dias tem no mês que você selecionou, por exemplo se você selecionou o mês de março, ele te mostrará que o mês tem 31 dias. Além do mais, ele exibi essa informação na tela e retorna as pastas anteriores.


```markdown
@echo off

if not exist "%1" (
    mkdir "%1"
)
cd "%1"
if not exist "%2" (
    mkdir "%2"
)
cd "%2"
set mes=%2
echo oi
if %mes%==1 set dias=31
if %mes%==2 set dias=28
if %mes%==3 set dias=31
if %mes%==4 set dias=30
if %mes%==5 set dias=31
if %mes%==6 set dias=30
if %mes%==7 set dias=31
if %mes%==8 set dias=31
if %mes%==9 set dias=30
if %mes%==10 set dias=31
if %mes%==11 set dias=30
if %mes%==12 set dias=31

echo o numero de dias %dias% no mes %mes%
cd ..
cd ..
```

# Passo a passo do script
```markdown
@echo off
```
Impede que os comandos do script sejam exibidos na tela durante a execução, deixando apenas as saídas desejadas (como mensagens do echo).

```markdown
if not exist "%1" (
    mkdir "%1"
)
cd "%1"

if not exist "%2" (
    mkdir "%2"
)
```

--> if not exist "%1" → Verifica se o diretório passado como primeiro argumento (%1) não existe.

--> mkdir "%1" → Se o diretório não existir, ele o cria.

--> cd "%1" → Entra no diretório criado (ou no já existente).

--> if not exist "%2" → Verifica se o diretório passado como segundo argumento (%2) não existe.

--> mkdir "%2" → Se não existir, ele cria o segundo diretório.


```markdown
cd "%2"
set mes=%2
echo oi
```

--> icd "%2" → Tenta entrar no diretório com o nome passado como segundo argumento (%2).

--> iset mes=%2 → Define a variável mes com o valor de %2.

--> iecho oi → Exibe a mensagem "oi" no terminal.


```markdown
if %mes%==1 set dias=31
if %mes%==2 set dias=28
if %mes%==3 set dias=31
if %mes%==4 set dias=30
if %mes%==5 set dias=31
if %mes%==6 set dias=30
if %mes%==7 set dias=31
if %mes%==8 set dias=31
if %mes%==9 set dias=30
if %mes%==10 set dias=31
if %mes%==11 set dias=30
if %mes%==12 set dias=31
```

--> Esse código verifica o valor da variável %mes% e define a quantidade de dias do mês correspondente. Se %mes% for 1 (janeiro), ele define dias=31; se for 2 (fevereiro), define dias=28, e assim por diante.

# Conclusão
O script Batch desenvolvido automatiza a verificação do número de dias de um mês. Ele recebe o mês e o ano como parâmetros, calcula a quantidade de dias no mês e exibe o resultado.

Objetivo: Calcular os dias de qualquer mês.
Aprendizado: Manipulação de variáveis e estruturas condicionais em Batch scripting.
