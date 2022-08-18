# Enviar e receber arquivos via SSH

Quem trabalha com SSH sabe que uma hora ou outra precisa mandar ou baixar do servidor. Com acessos do SSH, fazer isso é bem simples e vou explicar nesse artigo como fazer usando o comando SCP.

## O que é SPC?
SPC é abreviação de Secure Copy, que é um protocolo de rede para transfrência de arquivos utilizando encriptação SSH. Ou seja, você vai precisar apenas de um usuário e senha SSH para enviar ou receber arquivos.

## Como usar

Sem enrolação, vou colocar alguns exemplos de como utilizar o comando.


### Copiando arquivo remoto para máquina local

```
scp usuarioMaquinaRemota@ipDaMaquinaRemota:/home/diretorioRemoto/arquivo.txt /home/diretoriolocal/
```

### Copiando arquivo local para um servidor remoto

```
scp /home/diretorioLocal/arquivo.txt user@ipDaMaquinaRemota:/home/diretorioRemoto/arquivo.txt
```


### Copiando diretórios completos (com subpastas)

Nesse caso, vamos usar o atributo `-r`, que tornará a operação recursiva.
Além disso, devemos setar diretórios e não mais arquivos isolados.
Veja o exemplo:

```
scp -r usuarioMaquinaRemota@ipDaMaquinaRemota:/home/diretorioRemoto/pasta/ /home/diretorioLocal/
```

É isso aí.

@tihhgoncalves

