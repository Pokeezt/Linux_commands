

# Entender e usar as ferramentas essenciais

* Abrir um terminal, pode ser Kitty, Alacritty, ou outro.

# Acessar um prompt shell e emitir comandos

```bash
whoami        # mostra o usuário atual
pwd           # mostra o diretório atual (ex: /home/usuario)
date          # mostra a data e a hora atuais
hostname      # mostra o nome do sistema
```

## `>` Redirecionamento de entrada e saída

Cria um arquivo com o texto. Se o arquivo já existir, ele **apaga o conteúdo antigo** e escreve o novo.

```bash
echo "Olá mundo" > helloworld.txt      # "Olá mundo" será salvo dentro do helloworld.txt
```

Se usar `>` novamente:

```bash
echo "Hello World" > helloworld.txt    # Vai apagar o texto anterior e escrever "Hello World"
```

## `>>` (redirecionamento de saída, acrescenta ao final)

Igual ao `>`, mas **não apaga** o que já estava no arquivo. Ele **acrescenta no final**.

```bash
echo "Como você está?" >> helloworld.txt    # Adiciona a frase como nova linha
```

⚠️ Se esquecer de fechar as aspas, por exemplo:

```bash
echo "Como você está >> helloworld.txt"
```

O terminal vai entender que você **não terminou a frase** e vai ficar esperando:

```
>
```

Se isso acontecer, significa que **faltou fechar a aspa (`"`)**.

👉 Para **sair disso**, pressione `CTRL + C`.

## Ver o conteúdo do arquivo

Use `cat` para ver o que está dentro:

```bash
cat > helloworld.txt
```
Pode usar outro jeito assim:
```bash
cat helloworld.txt
```
É praticamente a mesma coisa.
Ambos mostram o conteúdo do arquivo na tela.


⚠️ Mas internamente há uma diferença sutil.
`cat helloworld.txt`: o cat acessa o arquivo diretamente.

`cat < helloworld.txt`: o shell abre o arquivo, e o cat só lê da entrada padrão.
