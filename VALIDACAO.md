# Matriz de validação do portfólio

**Fotografia documental de 23/11/2026.** Consulte a data e o SHA de cada execução antes de concluir que um teste ainda está válido. Os cinco aplicativos têm CI e demonstração web; o perfil é documentação. **Esta matriz distingue o que foi efetivamente testado e o que requer acesso/consentimento externo.**

## Níveis de evidência

| Nível | Significado |
|---|---|
| DOC | Comportamento descrito em fonte oficial, sem teste em ambiente real |
| SYNTH | Reproduzido com fixtures sintéticas, simulação ou navegador E2E |
| REAL | Reproduzido em serviço, dispositivo ou assistência real, com autorização |
| HOMOLOGADO | Fornecedor confirmou formalmente a integração necessária |
| INDETERMINADO | Não há fonte/ambiente/relato suficiente |

**DOC e SYNTH não equivalem a REAL.** Uma CI verde valida o código sob as condições do pipeline, não a compatibilidade universal. Não publique extratos bancários, HAR originais, fotos/endereços reais, tokens ou identificadores privados para provar uma verificação.

## Bloqueios e procedimentos por projeto

| Projeto | Comprovado até agora | Evidência externa faltante | Acompanhamento |
|---|---|---|---|
| [Fecha a Conta](https://github.com/ykauttiz/fecha-a-conta) | SYNTH: cálculo em centavos, importação, divergências, CSV, backup e navegadores automatizados | REAL: cabeçalhos e granularidade autorizados de exportações iFood/99Food, comparação com totais independentes; HOMOLOGADO: Financial API somente com credenciais e aprovação | [Issue #1](https://github.com/ykauttiz/fecha-a-conta/issues/1) |
| [Porta Fechada](https://github.com/ykauttiz/porta-fechada) | DOC + SYNTH: permissões e threads com fixtures, simulação de regras e CI | REAL: observar resultado de leitura/envio em servidor Discord e contas de teste autorizados | [Issue #1](https://github.com/ykauttiz/porta-fechada/issues/1) |
| [Últimos 50 Metros](https://github.com/ykauttiz/ultimos-50-metros) | SYNTH: localização simulada (inclusive negada), backup, erro de quota e navegação offline em navegador emulado | REAL: GPS físico, comportamento da precisão, uso offline continuado, persistência e restauração em celular físico | [Issue #1](https://github.com/ykauttiz/ultimos-50-metros/issues/1) |
| [Contratempo](https://github.com/ykauttiz/contratempo) | SYNTH: LRC, edição, playback e navegação por teclado em Chromium/Firefox | REAL: NVDA/Firefox ou TalkBack/Chrome e ensaio longo com usuário/testador consentido | [Issue #2](https://github.com/ykauttiz/contratempo/issues/2) |
| [Rastro Curto](https://github.com/ykauttiz/rastro-curto) | SYNTH: histogramas, percentuais, exportação somente agregada, dados HAR fictícios | REAL: interpretação e utilidade do boletim por equipe de suporte/QA | [Issue #5](https://github.com/ykauttiz/rastro-curto/issues/5) |

## Fontes confirmadas e consequências

**iFood** — [Homologação do Financial](https://developer.ifood.com.br/en-US/docs/food/guides/modules/financial/homologation): o módulo tem Reconciliation e Settlement, cadastro profissional com CNPJ e homologação separada para produção. Não infira que a exportação de CSV do Portal do Parceiro tenha os mesmos campos da API. Adapte apenas a partir de contrato/layout rastreável e teste sintético em centavos.

**99Food** — [Vitrine Open Delivery](https://aderentes.opendelivery.com.br/companies/68f696345e89f79a1563008a): há integrações de pedidos/merchant, portal de desenvolvedores e sandbox; a fonte **não confirma** exportação bancária ou API financeira homologada. Não invente uma.

**Discord** — [Threads](https://github.com/discord/discord-api-docs/blob/main/developers/topics/threads.mdx) e [Permissões](https://github.com/discord/discord-api-docs/blob/main/developers/topics/permissions.mdx): envio em threads depende de SEND_MESSAGES_IN_THREADS, não SEND_MESSAGES; private threads exigem convite ou gerenciamento; VIEW_CHANNEL no pai continua necessário. Essas regras documentais sustentam testes sintéticos, não autorizam acesso a servidores.

**Navegador** — [Playwright emulation](https://playwright.dev/python/docs/emulation) simula localização e offline. [Geolocation API](https://developer.mozilla.org/en-US/docs/Web/API/Geolocation_API) exige permissão. [Persistência](https://developer.mozilla.org/en-US/docs/Web/API/Storage_API/Storage_quotas_and_eviction_criteria) avisa que armazenamento local best-effort pode ser removido, exigindo backup.

**Acessibilidade** — [W3C](https://w3c.github.io/wcag/conformance-challenges/): automação identifica falhas, mas avaliação de leitura, teclado, áudio, foco e operabilidade completa inclui testes humanos.

## Próximo ciclo: o que conta como concluído

1. **Reproduzível:** documento de entrada e saída esperada (sempre sintética), versão da origem, passo a passo mínimo.
2. **Teste automatizado:** validações positivas, negativas, limites e regressões; identificação de SHA, navegador/versão e relatório da execução.
3. **Publicação:** PR mergeável com revisão e CI concluída; confirmação separada na main e Pages. Release etiquetada só se realmente criada.
4. **Teste externo:** responsável com ambiente e autorização, resultado observado e data; compartilhar somente relatório anonimizado. Caso falte, marcar **bloqueado — aguardando evidência externa** e manter issue aberta.
5. **Produto:** segurança, precisão e acessibilidade antes de animações ou novas funcionalidades. Evitar reescritas e dependências sem benefício mensurável.

O prompt operacional completo usado para orientar a manutenção está em [PROMPT_AUTOMACAO.md](PROMPT_AUTOMACAO.md). Esta matriz não contém segredos nem dados privados; é a referência compartilhada entre execuções.
