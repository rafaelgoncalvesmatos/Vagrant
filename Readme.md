# Vagrant

Este repositorio vem para auxiliar na documentacao dos estudos referente a está solução da Hashicorp para provisionamento de recursos.

Muito fácil para construção de ambiente de POC.

## Indice

1. Basico
    * [basico1](./vagrant_code/01-Basico/basico1/)
    * [basico2](./vagrant_code/01-Basico/basico2/)
    * [basico3](./vagrant_code/01-Basico/basico3/)

2. Intermediario
    * [intermediario1](./vagrant_code/02-Intermediario/inter1/)
    * [intermediario2](./vagrant_code/02-Intermediario/inter2/)
    * [intermediario3](./vagrant_code/02-Intermediario/inter3/)
    * [intermediario4](./vagrant_code/02-Intermediario/inter4/)
    * [intermediario5](./vagrant_code/02-Intermediario/inter5/)

3. Avancado
    * [avancado1](./vagrant_code/03-Avancado/avanc1/)
    * [avancado2](./vagrant_code/03-Avancado/avanc2/)
    
4. [Plugins](./vagrant_code/97-plugins/plug1)

5. Truques
    * [truque1](./vagrant_code/98-truques/truque01/)
    * [truque2](./vagrant_code/98-truques/truque02/)

6. Provision
    * [provision1](./vagrant_code/99-provision/prov01/)

## Ajuda

Segue alguns links uteis para achar a box que se adeque a sua necessidade:

> https://app.vagrantup.com/boxes/search

## Iniciando maquina

Criar o arquivo com **Vagrantfile** que contem as configuracoes da nossa VM, neste caso ele ira definir que a box utilizada sera o centos 7:

```
$ vagrant init -m centos/7
```

O parametro -m e de minimal, nao contera os comentarios padroes.


Enfim, para iniciar a maquina apenas entre no diretorio de onde esta o arquivo **Vagrantfile** e levante a maquina virtual.

```
$ vagrant up
```

![](.images/img1.png)

## Acesso a maquina

Para acesso com este comando: 

```
$ vagrant ssh
```

Uma maquina especifica:

``` 
$ vagrant ssh elastic01
```

ou 

```
$ vagrant ssh a44
```

## Desligando maquina

Para desligamento apenas digite no mesmo diretorio:

```
$ vagrant halt
```

Para desligar uma maquina especifica obtenha o ID:

```
$ vagrant global-status
id       name    provider   state    directory                                                                   
-----------------------------------------------------------------------------------------------------------------
a44814a  default virtualbox running /home/rafa/Devops/github/Vagrant_exemplos/vagrant_code/01 - Simples/basico2 
 
The above shows information about all known Vagrant environments
on this machine. This data is cached and may not be completely
up-to-date (use "vagrant global-status --prune" to prune invalid
entries). To interact with any of the machines, you can go to that
directory and run Vagrant, or you can use the ID directly with
Vagrant commands from any directory. For example:
"vagrant destroy 1a2b3c4d"
```

Executando:

```
$ vagrant halt a44
```

## Destruindo

Para destruicao execute:

```
$ vagrant destroy 
```

Ou uma maquina especifica:

```
$ vagrant destroy a444
```

Para nao perguntar se vc tem certeza de remover execute com parametro **-f**:

```
$ vagrant destroy -f 
```

## Conclusao

Uma ferramente de curto aprendizado e com muito resultado para POC, Lab, estudos e documentacao de infraestrutura.
