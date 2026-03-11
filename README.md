# Documentação: Circuito Divisor de Tensao 3s
Oie! Esta é uma documentação para um projeto da aula de Sistemas Embarcados, referente a um prototipo de circuito de um divisor de tensao 3s. 
Este circuito se refere a uma Fonte de energia de 12v, que serve para estabilizar a energia que vem de uma tomada (ou transformador) e alimentar um dispositivo. Hoje irei explicar como este projeto funciona, trazendo sua lsita de componentes e funcionalidades. 

## Especificações do Projeto

O trabalho possui os seguintes requisitos técnicos definidos:

- Placa retangular com 40 mm de altura e 80 mm de largura

- Conector macho representando a saída secundária do transformador

- **Desenvolvimento do circuito em três modos**

  1 .Esquemático

  2. PCB

  3. Visualização 3D

- Capturas de tela do circuito nos três modos

- Utilização dos mesmos valores de resistores e capacitores do simulador

- As trilhas do circuito devem estar posicionadas na parte inferior da placa (Bottom Layer), representadas pela cor azul

- O projeto deve ser publicado no GitHub, contendo documentação detalhada sobre o funcionamento de cada componente do circuito.

  
##Componentes Utilizados

1. Regulador de Tensão 7812

O que é:
O 7812 é um circuito integrado regulador de tensão da família 78xx, utilizado para fornecer tensão positiva fixa.

Função:
Recebe uma tensão contínua ainda com pequenas oscilações e a regula para uma saída estável de 12V.

Importância no circuito:
Este componente garante que o dispositivo alimentado receba sempre a tensão correta, mesmo que ocorram pequenas variações na entrada.

Sinal da onda:
Entrada: tensão contínua com pequenas ondulações (ripple)
Saída: tensão contínua estabilizada (linha DC praticamente reta)

--- 

2. Ponte Retificadora (Bridge)

O que é:
Um conjunto de quatro diodos organizados em formato de ponte.

Função:
Converte a tensão AC (corrente alternada) em DC pulsante, realizando a retificação de onda completa.

Importância no circuito:
Permite que a energia proveniente do transformador possa ser utilizada por circuitos eletrônicos que operam com corrente contínua.

Sinal da onda:
Entrada: onda senoidal AC
Saída: onda pulsante positiva

---

3. Capacitor Eletrolítico (CAP-ELEC)

O que é:
Um capacitor de alta capacitância e polarizado, utilizado para armazenamento de carga.

Função:
Filtrar a tensão pulsante, reduzindo as variações da tensão entre os pulsos.

Importância no circuito:
Suaviza o sinal retificado, reduzindo o ripple e tornando a tensão mais estável antes da regulação.

Sinal da onda:
Transforma a onda pulsante em uma tensão contínua com pequena ondulação (ripple).

---

4. Capacitor Cerâmico (CAP)

O que é:
Um capacitor de baixa capacitância utilizado para desacoplamento.

Função:
Filtrar ruídos de alta frequência e interferências elétricas.

Importância no circuito:
Ajuda a manter a estabilidade do regulador 7812, evitando oscilações e interferências no circuito.

Sinal da onda:
Remove pequenos ruídos e picos de tensão presentes na linha DC.

---

5. Conectores (CONN-SIL2 / SIL-100-02)

O que são:
Terminais de conexão utilizados para entrada e saída de energia do circuito.

Função:

Conector de entrada: recebe a tensão AC do transformador

Conector de saída: fornece a tensão 12V DC para a carga

Importância no circuito:
Permitem conexões externas de forma prática e segura, sem necessidade de soldagem direta na placa.

Sinal da onda:

Entrada: tensão AC senoidal
Saída: tensão DC estabilizada em 12V

---

6. LED (Diodo Emissor de Luz)

O que é:
Um dispositivo semicondutor que emite luz quando percorrido por corrente elétrica.

Função:
Indicar visualmente quando o circuito está energizado.

Importância no circuito:
Serve como indicador de funcionamento, permitindo ao usuário verificar rapidamente se a placa está ativa.

Sinal da onda:
Opera com tensão 12V DC, emitindo luz constante.

---

7. Resistor (MINRES120K)

O que é:
Componente passivo responsável por limitar a corrente elétrica.

Função:
Controlar a corrente que passa pelo LED.

Importância no circuito:
Evita que o LED receba corrente excessiva, o que poderia causar sua queima.

Sinal da onda:
Mantém a tensão contínua, mas limita a corrente no circuito do LED.

--- 
## Representações do Projeto

Conforme solicitado, o circuito foi representado em três diferentes modos no software de desenvolvimento:

1 -> Esquemático (Schematic Capture)

O esquemático representa a estrutura lógica do circuito, mostrando como os componentes estão conectados eletricamente.

Nesta etapa são definidos:

os componentes utilizados

as conexões elétricas

a lógica de funcionamento do circuito

Também é possível realizar simulações para verificar se o circuito entrega corretamente a tensão esperada.

- esquematico: 
<img width="1159" height="307" alt="image" src="https://github.com/user-attachments/assets/214402cc-ca05-4a13-92a0-3ef7f769f2a4" />


2 -> Layout da PCB (ARES)

O layout da PCB representa o desenho físico da placa de circuito impresso.

Nesta etapa são definidos:

posição real dos componentes

trilhas de cobre que fazem as conexões

dimensões da placa

organização dos elementos na superfície

Todas as trilhas foram desenhadas na camada inferior da placa (Bottom Layer), conforme especificado.

- PCB Layout:
  <img width="1226" height="649" alt="image" src="https://github.com/user-attachments/assets/468f5e70-38ab-4156-b297-4ddd34ef313a" />

  

3 -> Visualização 3D

A visualização 3D permite observar como será o circuito após a montagem física.

Esse modo ajuda a verificar:

espaçamento entre componentes

orientação correta de conectores

aparência final da placa

- parte superior:
 <img width="1027" height="633" alt="image" src="https://github.com/user-attachments/assets/6c86dcc8-d6fb-4cdb-9ea3-36d45ca06994" />
 
  
- parte inferior:

<img width="978" height="514" alt="image" src="https://github.com/user-attachments/assets/852cc1d4-d055-4d93-8222-d002722d1e4f" />

