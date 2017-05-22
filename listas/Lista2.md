**Universidade Federal de Minas Gerais**

**Disciplina: DCC065 - Sistemas Operacionais**

**Professor: Flavio Vinicius Diniz de Figueiredo**

# Lista de Exercícios - Prova 2

## Memória: Hardware

1. [Silberschatz 8.1] Qual a diferença entre endereços lógicos e físicos?

1. [Silberschatz 8.3] Por que os tamanhos de página sempre são potência de 2?

1. Cite 2 vantagens de utilizar endereçamento hierárquico? Isto é, um diretório
   de páginas e uma tabela de páginas?

1. Qual o tamanho máximo de memória física possível em um sistema de 32 bits?
   E em um de 64 bits?

1. [Tanenbaum 3.4] Considere um sistema de troca de processos entre memória e
   disco no qual a memória é constituída de lacunas em ordem na memória:
   10 KB, 4 KB, 20KB, 18KB, 7KB,  9KB, 12KB e 15KB. Qual lacuna é ocupada
   quando solicitamos de forma sucessiva: 12, 10 e 9 KB respectivamente? Use
   os algoritmos: first fit, best fit, worst fit e next fit.

1. [Tanenbaum 3.18] Uma máquina tem um endereçamento virtual de 48 bits e um
   endereçamento físico de 32 bits. As páginas são de 8KB. Quantas entradas são
   necessárias na tabela de páginas?

1. [Silberschatz 8.13] Compare os esquemas de alocação contígua, segmentação
   pura e paginação pura com relação às questões a seguir:
   1. Fragmentação externa
   1. Fragmentação interna
   1. Compartilhamento

1. [Silberschatz 8.15] Explique por que sistemas operacionais móveis como iOS
   e Android não suportam permuta?

1. [Siberschatz 8.20] Supondo um tamanho de página de 1KB (2^10, com 2^22
   bits para tradução). Quais são os números de deslocamentos de página para as
   referências a seguir (fornecidas como decimais):
   1. 3085  (`0b00000000000000000000110000001101` --> `num = 0000000000000000000011 | off = 0000001101`)
   1. 42095
   1. 215201
   1. 650000
   1. 200001

1. [Siberschatz 8.24] Considera um sistema de computação com um endereço lógico
   de 32 bits e tamanho de página de 4KB. O sistema de 512MB de memória física.
   Quantas entradas haveria em cada um dos itens a seguir:
   1. Tabela de páginas de um único nível
   1. Tabela de páginas de dois níveis
   1. Tabela hash

1. [Siberschatz 8.25] Considera um sistema de paginação simples:
   1. Se uma referência para a memória gasta 50ns, quanto tempo leva uma
      referência para a memória paginada.
   1. Se a TLB tem 75% de acerto, qual será o tempo efetivo de acesso à
      memória? (Assuma que a TLB tem um custo de 2ns)

1. [Siberschatz 8.29] Qual a finalidade da paginação da tabela de páginas?

1. [Tanenbaum 3.10] Suponha que uma máquina tenha endereços virtuais de 48 bits
   e endereços físicos de 32 bits.
   1. Se as páginas são de 4KB, quantas entradas existem na tabela de páginas
      se a mesma for de 1 nível?
   1. Suponha que o mesmo sistema tenha uma TLB com 32 entradas. Assumindo
      um tempo de acesso de 10ns para a memória real e 2ns para a TLB, qual a
      efiácia do sistema?

## Memória: SO

1. [Siberschatz 9.1 - Resumida] Quando ocorrem os erros/faltas de pagina?
   Quais são os passos do SO para tratar as mesmas?

1. [Siberschatz 9.7]

1. [Siberschatz 9.10 - Alterada] Em um algoritmo ótimo pode ocorrer a anomalia
   de belady? Explique.

1. [Siberschatz 9.17 - Resumida] Quais as vantagens do copy on write? Como o SO
   e o hardware podem implementar o mesmo?

1. [Tanenbaum 3.20 - Reformulada] Imagine um compilador que vai observar todos
   os acessos de memória do código, gerando como saída as páginas que devem
   ser substituídas para implementar uma política de troca de páginas ótima.
   É possível gerar tal compilador? Explique por quê. O mesmo funciona quando
   o algoritmo de troca de páginas é global?

1. [Tanenbaum 3.22] Se o algoritmo FIFO é usado com quatro molduras de página
   e oito páginas virtuais, quantas faltas vão ocorrer para a sequência de
   acessos `01723277103`. Repita para LRU.

1. Um computador pequeno tem quatro molduras de página. No primeiro tique do
   relógio os bits R são `0111`. Os próximos tiques são: `1011`, `1010`,
   `1101`, `0010`, `1010`, `1100` e `0001`. Se o algoritmo de envelhecimento,
   aging, é usado com um contador de 8 bits. Quais os valores dos quatro
   contadores após o último tique.

1. [Tanenbaum 3.28] Um computador tem quatro molduras de página. O tempo de
   carregamento da página na memória, o instante do último acesso e os bits
   `R e M` para cada página são mostrados a seguir:

    | Página | Carregado | Última ref. | R | M |
    |--------|-----------|-------------|---|---|
    | 0      | 126       | 280         | 1 | 0 |
    | 1      | 230       | 265         | 0 | 1 |
    | 2      | 140       | 270         | 0 | 0 |
    | 3      | 110       | 285         | 1 | 1 |

    1. Qual página será trocada pelo NRU?
    1. FIFO?
    1. LRU
    1. Segunda chance?
