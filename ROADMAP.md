# Projetos publicados e próximos passos

Revisão de 21 de novembro de 2026. Os links de verificação apontam para a execução correspondente à entrega. Os artefatos de cada execução incluem capturas com 320, 375 e 1280 pixels de largura em Chromium e Firefox.

| Projeto | Experimente | Testes e capturas desta revisão |
|---|---|---|
| Contratempo | [Sala de ensaio](https://ykauttiz.github.io/contratempo/) | [Execução](https://github.com/ykauttiz/contratempo/actions/runs/44937617422) |
| Fecha a Conta | [Conferência de repasses](https://ykauttiz.github.io/fecha-a-conta/) | [Execução](https://github.com/ykauttiz/fecha-a-conta/actions/runs/44937614612) |
| Porta Fechada | [Simulador de canais de texto](https://ykauttiz.github.io/porta-fechada/) | [Execução](https://github.com/ykauttiz/porta-fechada/actions/runs/44937612699) |
| Últimos 50 Metros | [Caderno de campo](https://ykauttiz.github.io/ultimos-50-metros/) | [Execução](https://github.com/ykauttiz/ultimos-50-metros/actions/runs/44910145718) |

## Contratempo

A faixa de exemplo permite experimentar repetição A/B, busca de versos, forma de onda e velocidade. Com uma gravação local, também dá para marcar versos, ajustar sincronização, exportar LRC, SRT e WebVTT e apresentar a letra. Ensaios nomeados ficam no navegador. O backup de sessão guarda as marcações e os ajustes. Para retomar, selecione o áudio original.

No treino progressivo, escolha duas ou quatro voltas no trecho. O contador acompanha as repetições e a velocidade sobe ao próximo nível disponível.

A suíte verifica 10 mil marcações e navegação por teclado até o último resultado. A validação de experiência em ensaios reais e com tecnologia assistiva continua aberta.

## Fecha a Conta

O fechamento mantém a origem dos lançamentos, agrupa pedidos e lotes e calcula valores em centavos. Na demonstração, o pedido 0019 tem diferença de R$ 1,50. A tabela explica o valor até a linha do CSV. É possível revisar diferenças, aplicar filtros, comparar lojas e plataformas e exportar evidências, impressão e backup. Os modelos de mapeamento podem ser reaproveitados com o mesmo cabeçalho, plataforma e tipo de arquivo.

O resumo para impressão segue os filtros da tela. Use-o para guardar o fechamento de uma loja ou plataforma e conferir os grupos incluídos.

O CSV de evidências neutraliza prefixos de fórmula ASCII, caracteres de controle e variantes Unicode conhecidas antes de chegar à planilha.

Para validar um importador nativo de iFood ou 99Food, ainda faltam extratos anonimizados, a versão do layout e um resultado esperado para comparação. A integração direta com a API depende de acesso oficial. A taxa configurável atual cobre a comissão percentual documentada. Contratos com outras fórmulas precisam de casos próprios.

## Porta Fechada

O motor compara duas configurações de canais de texto, testa leitura e envio para os membros e cargos declarados e identifica a etapa que alterou a decisão. A interface e a CLI trabalham com exemplos ou JSON local. O painel filtra os quatro resultados e os relatórios exportam a comparação completa. O CI registra a cobertura da suíte.

A matriz por membro compara leitura e envio por canal e conjunto de cargos. O histórico local guarda comparações nomeadas para reabrir ou remover depois. Na tabela, cada etapa decisiva pode ser expandida para conferir o resultado intermediário de cada sobrescrita aplicável. O relatório JSON acompanha o mesmo percurso. O formato 2 permite simular threads públicas e privadas, permissões do canal pai, convites, bloqueio e arquivamento. Uma integração de leitura com um servidor real depende de uma aplicação autorizada e de um servidor de teste. O simulador local já pode ser usado isoladamente.

O CSV de auditoria aplica a mesma neutralização de fórmulas a nomes de regras, canais, membros e cargos fornecidos pelo usuário.

## Últimos 50 Metros

O caderno diferencia vistoria, barreira, correção e verificação em campo. Aceita coordenadas manuais ou posição solicitada pelo usuário, mostra a precisão informada e permite revisar antes de salvar. Há fila por prioridade, comparação de visitas, histórico local, restauração de backup, uso offline preparado, impressão e exportação GeoJSON.

A seleção também pode ser exportada em CSV. O aplicativo inclui manifesto, ícones e cache offline para instalação em navegadores compatíveis. O mapa esquemático mostra as posições relativas sem baixar mapas de terceiros. Cada ponto aceita seleção pelo teclado. Fotos adicionadas pelo formulário são reduzidas e recodificadas no aparelho e podem ser recuperadas pelo backup JSON. CSV e GeoJSON contêm apenas os dados da vistoria. Sincronização entre pessoas e agregações por região dependem de demanda de campo e de regras de privacidade. A localização foi testada com coordenadas simuladas. Precisão de GPS em campo depende do aparelho e do local.

Identificadores de pontos também são neutralizados no CSV quando começam com um prefixo que uma planilha pode interpretar como fórmula.

## Perfil e manutenção

[Portfólio interativo](https://ykauttiz.github.io/contratempo/portfolio/). Nas revisões visuais, preserve a identidade de cada ferramenta, os exemplos reproduzíveis, a leitura em telas estreitas e a preferência de movimento reduzido. Compare o tema claro e o escuro com o mesmo conteúdo. Use capturas do produto para mostrar uma tarefa real.


O perfil apresenta os quatro projetos, demonstrações, código e banner com variantes clara e escura. A manutenção semanal revisa falhas, testes, documentação, exemplos e demanda pública. Revisões futuras devem registrar a evidência para qualquer novo recurso, publicação ou integração. Os quatro projetos estão fixados no perfil. A edição v2026.11.21.1 está publicada em cada repositório. Feedback de usuários e desempenho em celulares físicos precisam de observações reais.

## Como experimentar e avaliar a edição de novembro

| Projeto | Experiência curta | Versão publicada |
|---|---|---|
| Contratempo | Marque um trecho da faixa de exemplo e ouça a mudança de velocidade após duas voltas. | [Notas da versão](https://github.com/ykauttiz/contratempo/releases/tag/v2026.11.21.1) |
| Fecha a Conta | Isole o pedido 0019 da demonstração e confira a diferença no resumo impresso. | [Notas da versão](https://github.com/ykauttiz/fecha-a-conta/releases/tag/v2026.11.21.1) |
| Porta Fechada | Compare os exemplos de canal, salve o resultado e reabra a comparação pelo nome. | [Notas da versão](https://github.com/ykauttiz/porta-fechada/releases/tag/v2026.11.21.1) |
| Últimos 50 Metros | Cadastre dois pontos fictícios com coordenadas distintas e selecione cada vistoria no mapa. | [Notas da versão](https://github.com/ykauttiz/ultimos-50-metros/releases/tag/v2026.11.21.1) |

Para relatar um problema, informe o projeto, o navegador, os passos, o resultado esperado e o que aconteceu. Use dados fictícios em anexos públicos.

## Validação com usuários

- [Ensaio por teclado e leitor de tela](https://github.com/ykauttiz/contratempo/issues/2)
- [Layout de extrato e resultado esperado](https://github.com/ykauttiz/fecha-a-conta/issues/1)
- [Permissões de threads em um servidor de teste](https://github.com/ykauttiz/porta-fechada/issues/1)
- [GPS, uso offline e recuperação em celular](https://github.com/ykauttiz/ultimos-50-metros/issues/1)
