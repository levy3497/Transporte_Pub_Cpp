
---

## Projeto sugerido: **Simulador completo de um sistema de transporte público urbano**

### 1. **Descrição geral**

Um programa que simula uma cidade com linhas de ônibus, horários, passageiros e controle de tráfego. Ele deve permitir **adicionar/remover linhas, ônibus, passageiros**, simular movimento em tempo real e gerar relatórios de eficiência.

Você vai ter que criar **uma arquitetura grande**, tipo um “mini ERP de transporte público”, mas só em console ou GUI simples (opcional).

---

### 2. **Componentes principais**

#### a) Classes e objetos

* `Cidade` – contém todas as linhas, estações e ônibus.
* `Linha` – cada linha tem um número, lista de estações, horários e ônibus.
* `Onibus` – com capacidade, passageiros, posição atual.
* `Estacao` – nome, coordenadas, lista de passageiros esperando.
* `Passageiro` – nome, origem, destino, tempo de espera.
* `Horario` – pode ser uma classe para manipular horários de saída e chegada.

---

#### b) Funcionalidades do simulador

* **Simulação em tempo real** (ou em “ticks”):

  * Cada tick representa 1 minuto do dia.
  * Ônibus se movem entre estações.
  * Passageiros embarcam/desembarcam.
  * Atualizar tempo de espera de passageiros.

* **Gerenciamento**:

  * Adicionar/remover linhas, estações e ônibus.
  * Cadastrar passageiros.
  * Alterar horários dinamicamente.

* **Relatórios**:

  * Tempo médio de espera por estação.
  * Lotação média dos ônibus.
  * Linhas mais eficientes.

---

#### c) Arquivos e persistência

* Salvar e carregar dados de:

  * `linhas.txt` → informações das linhas e horários
  * `onibus.txt` → status dos ônibus
  * `passageiros.txt` → passageiros aguardando ou viajando
* Você vai praticar **fstream, ifstream, ofstream, parsing de CSV ou JSON simples**.

---

#### d) Multithreading (opcional, avançado)

* Um thread simula os ônibus.
* Outro thread atualiza relatórios.
* Um terceiro thread pode simular novos passageiros chegando aleatoriamente.

Isso força você a lidar com **mutex, locks e concorrência**, que é um nível avançado.

---

#### e) Interface

* **Console**: menus interativos com entrada e saída de dados.
* **Opcional GUI leve**: ncurses ou QT (se quiser algo visual, mas só se já tiver experiência).

---

### 3. **Conceitos de C++ que você vai usar**

* Classes e objetos complexos
* Herança e polimorfismo
* Smart pointers (`unique_ptr`, `shared_ptr`)
* STL: `vector`, `map`, `queue`, `set`
* Arquivos: leitura e escrita
* Multithreading (`thread`, `mutex`, `condition_variable`)
* Algoritmos de simulação e cálculo (tempos, distâncias)
* Tratamento de erros e exceções

---

### 4. **Como escalar o projeto**

* Comece com **uma linha e um ônibus**.
* Depois adicione múltiplas linhas, múltiplos ônibus.
* Depois simule centenas de passageiros.
* Por fim, implemente relatórios complexos e simulação avançada com threads.

---	
