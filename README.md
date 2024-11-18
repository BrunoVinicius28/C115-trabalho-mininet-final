# C115 - Trabalho Final com Mininet
Este repositório contém o trabalho prático desenvolvido na disciplina C115 tendo como objetivos a criação de uma topologia linear e a criação de uma topologia customizada no Mininet. Ele inclui a definição da topologia, inspeção de interfaces, testes de conectividade e análise de desempenho em diferentes topologias de rede.

## Objetivo
O trabalho explora a criação e o teste de topologias de rede no Mininet, sendo que na primeira parte foi configurada uma topologia linear com oito hosts (h1 a h8) e oito switches (s1 a s8) para realizar testes de largura de banda e conectividade TCP usando ferramentas como iperf. Já na segunda parte foi configurada uma topologia customizada com sete hosts (h1 a h7) e sete switches (s1 a s7). O objetivo é aplicar conceitos de redes de computadores na prática.

## Primeira parte: Implementação de Topologia Linear
A topologia utilizada na primeira parte foi uma topologia linear com os seguintes parâmetros:

+ Larguras de banda: 1, 5, 10, 15, 20, 25 e 30 Mbps
+ Endereços MAC padronizados para os hosts e switches

### Comando para criação da topologia considerando largura de banda de 30 Mbps:
```
sudo mn --topo linear,8 --mac --link tc,bw=30
```
#### Saída obtida:
![Simulação parte 1](simulacao_parte1.png)

## Inspecionando Interfaces, Endereços MAC, IP e Portas
Após a criação da topologia, foi possível inspecionar as interfaces de rede, endereços MAC e IP dos hosts e switches, utilizando os seguintes comandos:

### 1. Listar todos os nós:
![Simulação parte 2](simulacao_parte2.png)

### 2. Exibir interfaces de rede do host h1:
![Simulação parte 3](simulacao_parte3.png)

### 3. Exibir informações das interfaces do switch s1:
![Simulação parte 4](simulacao_parte4.png)
![Simulação parte 5](simulacao_parte5.png)
![Simulação parte 6](simulacao_parte6.png)
![Simulação parte 7](simulacao_parte7.png)

### 4. Verificar as portas e mapeamentos dos hosts e switches:
![Simulação parte 8](simulacao_parte8.png)

### Teste de Ping
Para verificar a conectividade entre diferentes nós na topologia, foram realizados testes de ping entre os hosts:

#### h1 e h2:
##### Host h1:
![Simulação parte 9](simulacao_parte9.png)

##### Host h2:
![Simulação parte 10](simulacao_parte10.png) 

![Simulação parte 11](simulacao_parte11.png)

#### h1 e h3:
##### Host h1:
![Simulação parte 12](simulacao_parte12.png)

##### Host h3:
![Simulação parte 13](simulacao_parte13.png)

![Simulação parte 14](simulacao_parte14.png)

Abaixo, foi criado um desenho com as principais informações da topologia: 

![Simulação parte 36](simulacao_parte36.png)

### Teste de Largura de Banda com Iperf
Os testes de largura de banda TCP foram realizados entre o host 1 (servidor) e o host 2 (cliente) com  larguras de banda de 1, 5, 10, 15, 20, 25 e 30 Mbps usando a ferramenta iperf.

### Teste com 1 Mbps
#### Servidor TCP no host 1 (porta 5555):
![Simulação parte 15](simulacao_parte15.png)

#### Cliente TCP no host 2, enviando dados por 15 segundos, com relatórios a cada 1 segundo e largura de banda de 1 Mbps:
![Simulação parte 16](simulacao_parte16.png)

Para uma visualização clara dos resultados de desempenho, foi gerado um gráfico utilizando o Gnuplot, que exibe o throughput (largura de banda) em Mbps a cada segundo durante o teste de 15 segundos.

#### Gráfico de Desempenho do Cliente TCP:
![Simulação parte 17](simulacao_parte17.png)

Este gráfico mostra a variação da largura de banda ao longo do tempo durante o teste, oferecendo uma visão detalhada da performance da comunicação TCP entre os hosts.

### Teste com 5 Mbps
#### Servidor TCP no host 1 (porta 5555):
![Simulação parte 18](simulacao_parte18.png)

#### Cliente TCP no host 2, enviando dados por 15 segundos, com relatórios a cada 1 segundo e largura de banda de 5 Mbps:
![Simulação parte 19](simulacao_parte19.png)

Para uma visualização clara dos resultados de desempenho, foi gerado um gráfico utilizando o Gnuplot, que exibe o throughput (largura de banda) em Mbps a cada segundo durante o teste de 15 segundos.

#### Gráfico de Desempenho do Cliente TCP:
![Simulação parte 20](simulacao_parte20.png)

Este gráfico mostra a variação da largura de banda ao longo do tempo durante o teste, oferecendo uma visão detalhada da performance da comunicação TCP entre os hosts.

### Teste com 10 Mbps
#### Servidor TCP no host 1 (porta 5555):
![Simulação parte 21](simulacao_parte21.png)

#### Cliente TCP no host 2, enviando dados por 15 segundos, com relatórios a cada 1 segundo e largura de banda de 10 Mbps:
![Simulação parte 22](simulacao_parte22.png)

Para uma visualização clara dos resultados de desempenho, foi gerado um gráfico utilizando o Gnuplot, que exibe o throughput (largura de banda) em Mbps a cada segundo durante o teste de 15 segundos.

#### Gráfico de Desempenho do Cliente TCP:
![Simulação parte 23](simulacao_parte23.png)

Este gráfico mostra a variação da largura de banda ao longo do tempo durante o teste, oferecendo uma visão detalhada da performance da comunicação TCP entre os hosts.

### Teste com 15 Mbps
#### Servidor TCP no host 1 (porta 5555):
![Simulação parte 24](simulacao_parte24.png)

#### Cliente TCP no host 2, enviando dados por 15 segundos, com relatórios a cada 1 segundo e largura de banda de 15 Mbps:
![Simulação parte 25](simulacao_parte25.png)

Para uma visualização clara dos resultados de desempenho, foi gerado um gráfico utilizando o Gnuplot, que exibe o throughput (largura de banda) em Mbps a cada segundo durante o teste de 15 segundos.

#### Gráfico de Desempenho do Cliente TCP:
![Simulação parte 26](simulacao_parte26.png)

Este gráfico mostra a variação da largura de banda ao longo do tempo durante o teste, oferecendo uma visão detalhada da performance da comunicação TCP entre os hosts.

### Teste com 20 Mbps
#### Servidor TCP no host 1 (porta 5555):
![Simulação parte 27](simulacao_parte27.png)

#### Cliente TCP no host 2, enviando dados por 15 segundos, com relatórios a cada 1 segundo e largura de banda de 20 Mbps:
![Simulação parte 28](simulacao_parte28.png)

Para uma visualização clara dos resultados de desempenho, foi gerado um gráfico utilizando o Gnuplot, que exibe o throughput (largura de banda) em Mbps a cada segundo durante o teste de 15 segundos.

#### Gráfico de Desempenho do Cliente TCP:
![Simulação parte 29](simulacao_parte29.png)

Este gráfico mostra a variação da largura de banda ao longo do tempo durante o teste, oferecendo uma visão detalhada da performance da comunicação TCP entre os hosts.

### Teste com 25 Mbps
#### Servidor TCP no host 1 (porta 5555):
![Simulação parte 30](simulacao_parte30.png)

#### Cliente TCP no host 2, enviando dados por 15 segundos, com relatórios a cada 1 segundo e largura de banda de 25 Mbps:
![Simulação parte 31](simulacao_parte31.png)

Para uma visualização clara dos resultados de desempenho, foi gerado um gráfico utilizando o Gnuplot, que exibe o throughput (largura de banda) em Mbps a cada segundo durante o teste de 15 segundos.

#### Gráfico de Desempenho do Cliente TCP:
![Simulação parte 32](simulacao_parte32.png)

Este gráfico mostra a variação da largura de banda ao longo do tempo durante o teste, oferecendo uma visão detalhada da performance da comunicação TCP entre os hosts.

### Teste com 30 Mbps
#### Servidor TCP no host 1 (porta 5555):
![Simulação parte 33](simulacao_parte33.png)

#### Cliente TCP no host 2, enviando dados por 15 segundos, com relatórios a cada 1 segundo e largura de banda de 30 Mbps:
![Simulação parte 34](simulacao_parte34.png)

Para uma visualização clara dos resultados de desempenho, foi gerado um gráfico utilizando o Gnuplot, que exibe o throughput (largura de banda) em Mbps a cada segundo durante o teste de 15 segundos.

#### Gráfico de Desempenho do Cliente TCP:
![Simulação parte 35](simulacao_parte35.png)

Este gráfico mostra a variação da largura de banda ao longo do tempo durante o teste, oferecendo uma visão detalhada da performance da comunicação TCP entre os hosts.

## Segunda parte: Implementação de Topologia Customizada
A topologia utilizada na segunda parte foi uma topologia customizada em Python de acordo com o layout fornecido com os seguintes parâmetros:

+ Endereços MAC padronizados para os hosts e switches
+ Controlador manual

### Comando para criação da topologia:
```
sudo mn --custom topo-7host-7sw.py --topo mytopo --controller=none --mac
```
#### Saída obtida:
![Simulação parte 37](simulacao_parte37.png)

O código Python com a topologia completa se encontra nos arquivos do repositório.

## Inspecionando Interfaces, Endereços MAC, IP e Portas
Após a criação da topologia, foi possível inspecionar as interfaces de rede, endereços MAC e IP dos hosts e switches, utilizando os seguintes comandos:

### 1. Listar todos os nós:
![Simulação parte 38](simulacao_parte38.png)

### 2. Exibir interfaces de rede do host h1:
![Simulação parte 39](simulacao_parte39.png)

### 3. Exibir informações das interfaces do switch s1:
![Simulação parte 40](simulacao_parte40.png)
![Simulação parte 41](simulacao_parte41.png)
![Simulação parte 42](simulacao_parte42.png)

### 4. Verificar as portas e mapeamentos dos hosts e switches:
![Simulação parte 43](simulacao_parte43.png)
![Simulação parte 44](simulacao_parte44.png)

Abaixo, foi criado um desenho com as principais informações da topologia: 

![Simulação parte 45](simulacao_parte45.png)

## Execução de testes de ping entre os diferentes nós:
Para validar a conectividade da rede, foi realizado testes de ping entre os diferentes hosts considerando os switches normais:

#### h6 e h7:
##### Host h6:
![Simulação parte 46](simulacao_parte46.png)

##### Host h7:
![Simulação parte 47](simulacao_parte47.png) 

![Simulação parte 48](simulacao_parte48.png)

#### h1 e h5:
##### Host h1:
![Simulação parte 49](simulacao_parte49.png)

##### Host h5:
![Simulação parte 50](simulacao_parte50.png) 

![Simulação parte 51](simulacao_parte51.png)

## Apagando Regras Anteriores e Criando Regras Baseadas em Endereços MAC
Para configurar a rede com regras baseadas em endereços MAC, foram apagadas todas as regras de fluxo existentes nos switches :
```
sudo ovs-ofctl del-flows s3
sudo ovs-ofctl del-flows s7
sudo ovs-ofctl del-flows s2
sudo ovs-ofctl del-flows s4
```
Após isso, foram adicionadas novas regras de fluxo baseadas em endereços MAC. Foram usados comandos para a configuraração de regras específicas que permitem a comunicação entre hosts dentro de um mesmo switch (h2 e h3), hosts passado por pelo menos dois switches (h6 e h7) e entre hosts distantes (h6 e h2). Ao final, foram realizados testes de ping entre os hosts:

#### h2 e h3:
##### Host h2:
![Simulação parte 52](simulacao_parte52.png)

##### Host h3:
![Simulação parte 53](simulacao_parte53.png)

![Simulação parte 54](simulacao_parte54.png)

#### h6 e h7:
##### Host h6:
![Simulação parte 55](simulacao_parte55.png)

##### Host h7:
![Simulação parte 56](simulacao_parte56.png)

![Simulação parte 57](simulacao_parte57.png)


#### h6 e h2:
##### Host h6:
![Simulação parte 58](simulacao_parte58.png)

##### Host h2:
![Simulação parte 59](simulacao_parte59.png)

![Simulação parte 60](simulacao_parte60.png)

## Contribuições
Contribuições são bem-vindas! Sinta-se à vontade para abrir uma issue ou enviar um pull request para melhorias e ajustes.

## Licença
Este projeto está licenciado sob a MIT License.
