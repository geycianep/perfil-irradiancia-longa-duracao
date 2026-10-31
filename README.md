# Perfil de irradiância para o ensaio de longa duração

Dados para reproduzir o perfil de irradiância utilizado no ensaio de operação em longa duração da tese **Proposta de Metodologias para Avaliação e Classificação do Desempenho de Inversores Fotovoltaicos**, de Geyciane Pinheiro de Lima, Universidade Estadual de Campinas (UNICAMP).

**[Baixar os arquivos da versão 1.0.0](https://github.com/geycianep/perfil-irradiancia-longa-duracao/releases/tag/v1.0.0)**

## Arquivos

| Arquivo | Conteúdo |
| --- | --- |
| [perfil_irradiancia_longa_duracao.csv](perfil_irradiancia_longa_duracao.csv) | Sequência completa, com tempo, irradiância e temperatura do módulo simulado. |
| [cloudyday11h25.irtp](cloudyday11h25.irtp) | Arquivo utilizado como fonte, preservado sem alterações. |
| [SHA256SUMS.txt](SHA256SUMS.txt) | Códigos SHA-256 para conferir a integridade dos dois arquivos. |

## Origem e preparação

O perfil foi fornecido como exemplo no software do simulador fotovoltaico e utilizado na campanha experimental da tese. Este repositório documenta e disponibiliza a sequência empregada; não atribui à autora da tese a criação do perfil original.

O arquivo `.irtp` contém duas colunas, separadas por tabulação: irradiância e temperatura. A conversão para CSV preserva a ordem e os valores de todos os pontos. Os separadores decimais do arquivo de origem, que incluem pontos e vírgulas, foram padronizados como ponto no CSV. Foi acrescentada apenas a coluna de tempo, com início em zero e passo de 1 s, conforme a aplicação descrita na tese. Não foram aplicadas suavização, interpolação, redução de pontos ou normalização dos valores.

## Estrutura do CSV

O arquivo usa codificação UTF-8, vírgula como separador de colunas e ponto como separador decimal. A primeira linha contém os nomes das variáveis.

| Coluna | Unidade | Descrição |
| --- | --- | --- |
| `tempo_s` | s | Tempo relativo, de 0 a 38.997 s, com passo de 1 s. |
| `irradiancia_W_m2` | W/m² | Irradiância programada no simulador fotovoltaico. |
| `temperatura_modulo_C` | °C | Temperatura do módulo simulado, mantida em 25 °C. Não corresponde à temperatura ambiente nem à temperatura do inversor. |

## Condições para reprodução

1. Aplicar a sequência completa, na ordem do arquivo, com um ponto por segundo.
2. Manter a temperatura do módulo simulado em 25 °C.
3. Configurar a curva fotovoltaica e as condições elétricas de acordo com o inversor avaliado e com o procedimento de operação em longa duração descrito na tese.
4. Utilizar a mesma sequência e o mesmo passo temporal para os equipamentos que serão comparados.

O CSV contém o perfil de entrada do ensaio. As potências medidas e os resultados de eficiência dos inversores não fazem parte deste conjunto de dados.

## Características da sequência

| Grandeza | Valor |
| --- | --- |
| Número de pontos | 38.998 |
| Passo temporal | 1 s |
| Intervalo entre o primeiro e o último ponto | 38.997 s, aproximadamente 10,83 h |
| Irradiância mínima | 9,50 W/m² |
| Irradiância máxima | 1.000 W/m² |
| Irradiância média aritmética | 589,412765 W/m² |
| Temperatura do módulo simulado | 25 °C |

## Referência

LIMA, Geyciane Pinheiro de. **Perfil de irradiância para o ensaio de longa duração de inversores fotovoltaicos**. Versão 1.0.0. GitHub, 2026. Disponível em: <https://github.com/geycianep/perfil-irradiancia-longa-duracao/releases/tag/v1.0.0>.

A referência identifica a organização e a disponibilização dos dados usados na tese. A origem do perfil está descrita acima. O arquivo `CITATION.cff` permite exportar a referência pelo GitHub.
