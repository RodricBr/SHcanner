
### Sumário:
- Scanner de portas usando NMAP <br>
- para os preguiçosos ou pra quem <br>
- não consegue decorar as opções (como eu) :) <br>


### Como executar SHcan.sh (Testado no [GitBash](https://git-scm.com/downloads) e Debian 10 Buster)
```bash
$ git clone https://github.com/rodricbr/shcan
$ cd shcan/;ls
$ chmod +x shcan.sh
$ sudo mv shcan.sh /usr/local/bin
$ sudo shcan.sh -h
```

### Como testar portas em conexão local usando netcat:
```bash
## 1º terminal
$ ifconfig
..: ip local, ex:192.168.0.1 :..
$ sudo nc -vlnp 123
..: escutando porta 123 :..

## 2º terminal
$ sudo shcan.sh 192.168.0.1 1-123
ou
$ sudo shcan.sh 192.168.0.1 1, 123
..: porta aberta: 123 :..
```

### Exemplos:
```bash
$ sudo shcan.sh 192.168.0.1 443
$ sudo shcan.sh 192.168.1.4 80-443 A
$ sudo shcan.sh 192.168.1.4 80,443,1337,22 P
```

### Nota:
O script não foi feito para ser útil ou
100% funcional, é um projeto pessoal
a fim de aprender sobre shell scripting
que decidi tornar público
