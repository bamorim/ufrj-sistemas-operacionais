EEL-770 Sistemas Operacionais
=============================

__Prof. Aloysio__

23/08/2013

2. Visão Geral
--------------

1. S.O. Computadores de Grande Porte
	* Ex: OS/390 (descendente do OS/360-IBM)
	* Unix
2. S.O. Servidores
	* Ex: Solaris, FreeBSD, Linux, Windows Server
3. S.O. Computadores Pessoais
	* Ex: Linux, FreeBSD, Windows8, MacOS
4. S.O. Computadores Portáteis
	* Ex: iOS, Android, Windows 8, Symbian(Nokia)
5. S.O. nós sensores
	* Ex: TinyOS
6. S.O. "smartcards"
	* Proprietarios
	* Muito Simples
	* Alguns orientados p/ Java

3. Conceitos
------------

### 3.1. Processos
Programas em excecução

Cosistem de:
* Programa executável
* Dados/Pilha
* Contexto de Execução do Programa (Salvo quando o processo é suspenso)
	* Contador de programa / apontador da pilha / registradores
	* Outras informações p/ excução do programa

--IMG1--

#### Tabela / Lista de processos
* Contem informações referentes a cada processo -> 1 elemento/processo
* Contexto é salvo durante a suspensão do processo
--IMG2--


Obs: Processo pode criar Processo Filho, guardando uma referencia para ele (pid)
--IMG3--

### 3.2. Arquivos

#### Arquivo
* Visão transparente dos discos e dos outros dispositivos de E/S
* "system calls"
	* Abrir/Fechar
	* Criar/Remover
	* Ler/Escrever

#### Diretório
* Agrupa arquivos
* Estrutura em árvore
* "path name" p/ cada arquivo a partir da raiz.

Ex: /Faculty/Prof.Brown/courses/cs101
--IMG4--

### 3.3. Comunicação entre Processos
* pipe
	* --IMG5--
	* "pseudo-arquivo"
	* Criar pipe -> "system call" -> pipe

### 3.4. "System Call"
* Primitivas do Sistema Operacional
* Operações indivisíveis
* --IMG6--
* Padrão de Primitivas: POSIX

4. Estrutura dos Sistemas Operacionais
--------------------------------------

1. Monolítico
--IMG7--

2. Piramide Unix
--IMG9--

5. Máquinas Virtuais
--------------------

Origem: IBM/370

|   OOO   |  OOO  |   OOO   | OOO |
|:-------:|:-----:|:-------:|:---:|
| Windows | Linux | Solaris | ... |
|           hypervisor         ||||

* Caso da IBM

| OS360 | CMS | CMS | CMS |
|:-----:|:---:|:---:|:---:|
|          VM370          |
|       Hardware 370   ||||

6. Modelo Cliente-Servidor
--------------------------

--IMG10--
--IMG11--