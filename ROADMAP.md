# Projetos publicados, auditoria e próximos passos

Atualização do portfólio: **23 de novembro de 2026**. Os links de CI abaixo apontam para o histórico de testes; cada execução deve ser conferida individualmente antes de afirmar que uma atualização foi aprovada. Testes automatizados não substituem validação com usuários e dados de campo consentidos.

| Projeto | Experimente | Testes e código |
|---|---|---|
| Contratempo | [Sala de ensaio](https://ykauttiz.github.io/contratempo/) | [CI](https://github.com/ykauttiz/contratempo/actions/workflows/contratempo-tests.yml) · [Repositório](https://github.com/ykauttiz/contratempo) |
| Fecha a Conta | [Conferência de repasses](https://ykauttiz.github.io/fecha-a-conta/) | [CI](https://github.com/ykauttiz/fecha-a-conta/actions/workflows/conferencia.yml) · [Repositório](https://github.com/ykauttiz/fecha-a-conta) |
| Porta Fechada | [Simulador de permissões](https://ykauttiz.github.io/porta-fechada/) | [CI](https://github.com/ykauttiz/porta-fechada/actions/workflows/verificar.yml) · [Repositório](https://github.com/ykauttiz/porta-fechada) |
| Últimos 50 Metros | [Caderno de campo](https://ykauttiz.github.io/ultimos-50-metros/) | [CI](https://github.com/ykauttiz/ultimos-50-metros/actions/workflows/verificar.yml) · [Repositório](https://github.com/ykauttiz/ultimos-50-metros) |
| Rastro Curto | [Boletim HAR](https://ykauttiz.github.io/rastro-curto/) | [CI](https://github.com/ykauttiz/rastro-curto/actions/workflows/test.yml) · [Repositório](https://github.com/ykauttiz/rastro-curto) |

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

## Rastro Curto

Ferramenta local para transformar arquivos HAR em **dois histogramas**: famílias HTTP e duração de cada requisição. É possível comparar os cenários A e B e baixar um boletim TXT com apenas contagens, sem exportar os detalhes individuais das requisições. O formato é deliberadamente limitado: ele não identifica a rota lenta, nem prova que uma mudança causou uma melhora. O arquivo HAR original pode conter segredos; nunca deve ser enviado ao GitHub ou a um chamado público.

O núcleo `core.js` valida a estrutura, limita a 50 mil entradas e não inclui URLs, cabeçalhos ou corpos na saída. Os testes abordam os limiares das faixas, códigos desconhecidos, entradas inválidas e ausência de dados sensíveis no resultado. Falta validação externa de utilidade com equipes de suporte.

[Issue ou sugestão para o Rastro Curto](https://github.com/ykauttiz/rastro-curto/issues) · [Release v0.1.0](https://github.com/ykauttiz/rastro-curto/releases/tag/v0.1.0)

## Perfil e manutenção

[Portfólio interativo](https://ykauttiz.github.io/contratempo/portfolio/). Nas revisões visuais, preserve a identidade de cada ferramenta, os exemplos reproduzíveis, a leitura em telas estreitas e a preferência de movimento reduzido. Compare o tema claro e o escuro com o mesmo conteúdo. Use capturas do produto para mostrar uma tarefa real.


O perfil apresenta **cinco ferramentas públicas**, demonstrações, código e banner com variantes clara e escura. A manutenção revisa falhas, testes, documentação, exemplos e demanda real. Versões e datas diferem entre os repositórios; consulte a aba Releases de cada um, em vez de presumir uma versão comum. Feedback de usuários e desempenho em celulares físicos ainda precisam de observações reais.

## Critérios de conclusão antes de novas versões

- **Integridade:** testes de regressão para importação, números, restauração e fluxo essencial.
- **Segurança:** usar dados inteiramente fictícios nas issues, exemplos, capturas e relatórios.
- **Acessibilidade:** validar teclado, contraste, foco e movimento reduzido com exemplos reais do próprio produto.
- **Publicação:** confirmar a CI da branch `main`, o deploy e, quando houver, a release gerada.
- **Validação externa:** diferenciar teste automatizado de execução com usuários, aparelho físico, serviços e permissões oficiais.

### Próximas verificações por projeto

| Projeto | Bloqueio atual | Critério de evidência |
|---|---|---|
| Contratempo | Leitor de tela e ensaio prolongado | Exercício reproduzido por teclado e tecnologia assistiva |
| Fecha a Conta | Layouts reais de iFood/99Food | CSV sintético fiel ao layout, totais esperados e teste |
| Porta Fechada | Paridade de threads e canais reais | Servidor e contas de teste autorizados |
| Últimos 50 Metros | GPS e armazenamento em campo | Aparelho real, internet desligada, backup restaurado |
| Rastro Curto | Utilidade do boletim em suporte | Chamado fictício avaliado por usuário de suporte |

## Validação com usuários

- [Ensaio por teclado e leitor de tela](https://github.com/ykauttiz/contratempo/issues/2)
- [Layout de extrato e resultado esperado](https://github.com/ykauttiz/fecha-a-conta/issues/1)
- [Permissões de threads em um servidor de teste](https://github.com/ykauttiz/porta-fechada/issues/1)
- [GPS, uso offline e recuperação em celular](https://github.com/ykauttiz/ultimos-50-metros/issues/1)
