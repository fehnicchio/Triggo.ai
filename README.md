# Triggo.ai
## Teste técnico para trainee


# 📊 Análise de Dados E-commerce - Olist


Projeto de análise de dados completo para explorar padrões de vendas, desempenho de entregas e satisfação de clientes no mercado brasileiro de e-commerce.

Para executar, basta clicar no link do Colab que irá abrir uma aba diretamente com o código em si, depois execute cada célular sequencialmente.
Lembre-se de criar uma pasta data e carregar os dataset dentro dela.

# Resultados:

## 1-Na primeira etapa, foi carregados os dataset e realizado a limpeza dos dados.

## 2- Tivemos os seguintes insights sobre os graficos:
A)Sazonalidade Clara: Picos em Novembro (Black Friday) e Dezembro (Natal)

Crescimento Anual: Volume aumenta a cada ano (2016: ~300 pedidos/mês → 2018: ~7.500 pedidos/mês)

Baixa em Janeiro: Queda pós-festas (comum no varejo)

B)Entrega Típica: 10-20 dias (moda em 15 dias)

Outliers Preocupantes: Pedidos levando até 60 dias

Meta x Realidade: 25% dos pedidos ultrapassam o prazo estimado

C)Existe uma relação positiva, mas não linear forte, entre distância e frete.A relação frete-distância na Olist é eficiente, mas pouco transparente. Enquanto a empresa demonstra capacidade de otimização logística, a baixa correlação sugere que políticas comerciais (como subsídios ou fretes promocionais) estão mascarando custos reais.

D)Produtos de maior ticket médio dominam

Categorias sazonais (ex: esportes) têm picos específicos

Beleza tem alta frequência de compra

E)Estados do Norte/Nordeste lideram em valor médio. Causa Provável: Compras menos frequentes porém de maior valor em regiões com menos opções físicas

## 3-A taxa de retenção atual reflete uma oportunidade urgente de otimização. Priorizar estratégias de fidelização pode transformar a base de clientes de transacional para recorrente

O modelo atual é viável para uso em cenários de baixo risco, mas requer melhorias para decisões críticas.

Pontos Fortes:

Alta Precisão para Não Atrasos (94%): Quando o modelo prevê que um pedido será entregue no prazo, está quase sempre correto.

Detecção Moderada de Atrasos (Recall 48%): Quase metade dos atrasos reais são identificados.

Pontos Fracos:

Baixa Precisão para Atrasos (15%): Apenas 15% das previsões de atraso estão corretas (85% são falsos positivos).

AUC-ROC Limitado (0.69): O modelo tem dificuldade em separar as classes de forma consistente.

### Insight para cada tipo de cliente:
Para clientes Inativos:

Comportamento:

Recência Alta (> 180 dias desde a última compra).

Frequência Baixa (1-2 pedidos).

Valor Monetário Baixo (média de R$ 150).

Estratégias de Marketing:

Campanhas de Reativação:

Enviar cupons de desconto personalizados (ex: "20% OFF na próxima compra").

Oferecer frete grátis para o próximo pedido.

Pesquisa de Satisfação:

Enviar pesquisa por e-mail para entender motivos da inatividade.

Conteúdo Relevante:

Compartilhar tutoriais de produtos ou lançamentos de categorias que o cliente comprou anteriormente.

Clientes Promissores:

Comportamento:

Recência Moderada (30-90 dias).

Frequência Média (2-3 pedidos).

Valor Monetário Crescente (média de R$ 300).

Estratégias de Marketing:

Programa de Fidelidade:

Oferecer pontos por compra que podem ser trocados por descontos.

Upsell de Produtos Complementares:

Recomendar acessórios relacionados a compras anteriores (ex: capinha para celular).

Ofertas Exclusivas:

Acesso antecipado a promoções de Black Friday ou Natal.

Clientes VIPs:

Comportamento:

Recência Baixa (< 15 dias).

Frequência Alta (5+ pedidos).

Valor Monetário Alto (média de R$ 1.200).

Estratégias de Marketing:

Benefícios Premium:

Programa VIP com atendente dedicado e entregas prioritárias.

Recompensas por Indicação:

Oferecer R$ 100 de crédito por cada amigo convertido.

Experiências Exclusivas:

Convites para eventos ou lançamentos de produtos.

Clientes em Risco:

Comportamento:

Recência Moderada-Alta (90-150 dias).

Frequência Decrescente (de 3 para 1 pedido nos últimos meses).

Valor Monetário Médio (R$ 400).

Estratégias de Marketing:

Ofertas Personalizadas:

Descontos em produtos similares aos que compraram anteriormente.

Comunicação Proativa:

E-mail com mensagem tipo "Sentimos sua falta! Aqui está um cupom de 15% OFF".

Garantia Estendida:

Oferecer garantia gratuita de 6 meses na próxima compra.

## 4-Top 3 Fatores que Impactam a Satisfação:

Tempo de Entrega (Correlação: -0.48)
Pedidos com atraso > 7 dias têm nota média de 2.8/5, enquanto entregas no prazo têm 4.6/5.

Ação: Priorizar transportadoras com SLA rigoroso para categorias de alta visibilidade (eletrônicos, móveis).

Categoria do Produto
Eletrônicos têm a menor nota média (3.2/5) devido a problemas de qualidade.

Livros têm a maior nota média (4.8/5).

Ação: Criar programa de controle de qualidade para vendedores de eletrônicos.

Valor do Pedido (Correlação: -0.18)
Pedidos acima de R$ 500 têm nota 12% menor que pedidos menores.

Causa: Expectativas mais altas não atendidas.

Ação: Oferecer suporte premium para compras acima de R$ 500.

1. Clone o repositório:
```bash
git clone https://github.com/seu-usuario/Triggo.ai.git
cd Triggo.ai
