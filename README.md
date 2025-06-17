# Cadeias-de-Markov

## Descrição:

Você tem acesso a uma base de dados contendo descrições textuais de assaltos ocorridos em diferentes cidades brasileiras. O objetivo é mapear esses dados em um grafo conexo, onde cada vértice representa uma cidade e as conexões entre elas são baseadas na similaridade semântica das descrições dos assaltos.

Para construir o grafo, recomenda-se utilizar a biblioteca sentence-transformers para gerar embeddings das descrições e calcular a similaridade do cosseno entre elas. Cidades com descrições similares devem ser conectadas. (Veja exemplo de uso neste link: https://sbert.net/).

## Tarefas:

1. Construção do grafo:

- Gere embeddings das descrições de assaltos.
- Calcule a similaridade do cosseno entre cidades.
- Conecte cidades com similaridade acima de um limiar (definido por você) para formar um grafo conexo.
- Use os graus dos vértices para montar a matriz de adjacência correspondente.

2. Análise com Cadeias de Markov:

- A partir da matriz de adjacência, construa uma matriz de transição estocástica.
- Use uma abordagem baseada em cadeias de Markov (como distribuição estacionária ou simulação de passos) para estimar as probabilidades de ocorrência futura de assaltos em cada cidade, com base na estrutura do grafo.

3. Identificar comunidades semânticas

- Aplique o algoritmo de Cluster Label Propagation sobre o grafo de similaridades.
- Analise os clusters resultantes, observando se há padrões linguísticos ou temáticos comuns entre as descrições agrupadas (por exemplo: roubos com uso de arma, furtos em estabelecimentos comerciais, assaltos noturnos, etc.).
- Cada cluster pode ser interpretado como um tipo predominante de crime com base nas descrições agrupadas.
