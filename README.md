# ULA-32BITS-VHDL
Projeto de ULA na linguagem de descrição VHDL 



Trabalho da ULA de 32 bits

Este trabalho pode ser feito em grupos de até 4 alunos. 

Descrever uma ULA (Unidade Lógica e Aritmética) de 32 bits em VHDL, que envolve projeto do somador e demais operações, detector de overflow, decodificador e multiplexador.
Livro Organização e Projeto de Computadores – A Interface Hardware / Software, Patterson & Hennessy.
Usar uma das seguintes ferramentas:
EDA Playground (versão via browser)
https://www.edaplayground.com/home (Links para um site externo.)
Symphony EDA
http://www.symphonyeda.com/ (Links para um site externo.) 
Intel Quartus Prime Lite Edition
https://www.intel.com/content/www/us/en/software/programmable/quartus-prime/overview.html (Links para um site externo.)
Xilinx ISE WebPACK
https://www.xilinx.com/products/design-tools/ise-design-suite/ise-webpack.html (Links para um site externo.)
Esta ULA deve realizar as seguintes operações: AND, OR, SOMA e SUBTRAÇÃO.
SOMA e AND já estão presentes no Teste 10. Falta adicionar OR e SUBTRAÇÃO.
Deve ter dois multiplexadores (MUXs: binvert e resultado), conforme projeto do livro de referência, e também um detector de overflow.
O MUX2x1 é o mesmo do Teste 6.
O Multiplexador resultado é um MUX4x1.
Fazer um decodificador para os 5 opcodes de instruções da figura abaixo.
A decodificação gera os sinais de binvert (bnegate) e operation.
Pode usar o decodificador do Teste 9.
Cada ULA de 1 bit deve ter a entrada Less e saída Set.
As entradas e saídas da ULA de 1 bit são as seguintes:
Entradas: a, b, Less, binvert, carryin, operação.
Saídas: resultado, set, overflow.
As entradas e saídas da ULA de 32 bits são as seguintes:
Entradas: a, b, bnegate, operação.
Saídas: zero, resultado, overflow.

Detalhe de projeto:
Cada bloco da ULA de 1 bit deve ser feito em VHDL independente. Portanto, haverá 1 VHDL para a operação SOMA, outro VHDL para MUX resultado, outro VHDL para overflow e assim por diante.
A ULA pode ter todas as operações em um único VHDL, tal como em Teste 10, que possui a SOMA e o AND no mesmo arquivo.vhd. 
Um VHDL ULA-1bit fará o port map dos demais códigos VHDLs.
Outro VHDL ULA-32bits fará o port map entre as ULAs de 1 bit.
Para testes de cada bloco ou dos blocos principais (ULAs) o grupo deve criar arquivos VHDL chamados test bench.
