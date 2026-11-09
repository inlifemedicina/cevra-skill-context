# Estado de retomada — 19/10/2026

## Decisões e escopo aprovado

Skill independente do Desktop, organização visual Mesa A e alvo funcional EDvid
completo foram aprovados. Esse alvo não foi reduzido aos cortes atuais; tampouco
é apresentado como entregue. Desenvolvimento incremental e integração futura
não autorizam banco compartilhado, migração implícita ou substituição do app.
A expansão do Vids original permanece pausada.

Os blocos entregues são offline, usando ferramentas locais já existentes, sem
instalação de dependências ou execução automática de agentes/providers.
Leitura/validação, preparação de revisão, edição temporária, checkpoint salvo e
exportação concluída têm significados distintos. Hashes provam consistência dos
bytes, não consentimento ou autenticação do produtor.

## Fontes técnicas locais — não publicadas aqui

| Entrega | Commit | Escopo |
|---|---|---|
| Fundação/Mesa A original | `52819481cd6e5b4ac908abf91840aae5fa0736aa` | Contratos, leitura limitada de pacote, preparação de revisão, prévia da fonte e cortes temporários com Undo/Redo |
| Sucessor durável/exportação | `442ae566c818726ef6868679b02dacc9520e0d71` | Clone separado, baseado em `5281948`, com salvamento/retomada explícitos e exportação de cortes |

Na auditoria de continuidade, ambos eram repositórios locais sem remoto
configurado. Seu código não foi copiado para este repositório de contexto nem
se presume disponível no remoto do app. Nenhum histórico Git desses projetos
foi importado. A foundation é baseline preservado, e a linha durável é a única ativa conforme
decisão posterior de 19/10. Preservar suas evidências e sessões, sem migração implícita.

## Entregas e limites

**Fundação/original:** contratos fechados, leitor TAR limitado, preparação pura
de revisões e prévia nativa da fonte; adicionar/aparar/remover/reordenar cortes,
journal temporário e Undo/Redo. Não é prévia da montagem renderizada nem garantia
de parada no frame exato. A leitura real de um pacote tem aceite técnico próprio;
esse aceite não estabelece todos os perfis, importação em app ou paridade completa.

**Durável/exportação:** checkpoint explícito com escrita atômica, controle de
concorrência e recuperação; recomposição da história e preparos; job de exportação
vinculado à revisão salva; QA, recibo e download verificado. O perfil é limitado a
SDR BT709 limited-range 8-bit square-pixel, clock/tamanho nativos, H.264 fast CRF20
e áudio opcional AAC 192k/48k mono/stereo. Perfis não suportados são recusados,
sem conversão silenciosa. Não é saída lossless. Abrir/reabrir não renderiza sozinho.

A implementação delimitada usa Python standard library, HTML/CSS/JavaScript,
player nativo do browser e FFmpeg existente. Isso não adota HyperFrames ou
OpenDesign. Apple-design foi consultado como referência documental, não instalado.
Uso local de ferramentas não estabelece autorização de redistribuição delas.

## Evidência histórica, sem reexecução nesta publicação

- Fundação/prévia/cortes: 8 testes novos e 8 de regressão aprovados; 12 cenários
  de browser em fixture própria e os mesmos cenários na fonte aceita; revisão
  independente sem achados abertos no delta. Progresso de relógio/decode não
  equivale a physical paint, avaliação de áudio/sync ou aceite humano.
- Durável/exportação: 13 testes novos aprovados na revisão independente;
  gates sintéticos native30, NTSC, VFR e lifecycle; 11 cenários novos de browser.
  Revisão final sem bloqueios remanescentes no delta. Um problema de regressão
  legada foi corrigido e o caso isolado passou; não alegar suíte ampla all-pass.
- A validação padrão de empacotamento da skill foi registrada como pendente por
  dependência ausente; nada foi instalado para contornar isso.

Esses números resumem relatórios locais anteriores. Não são nova execução,
auditoria integral, benchmark comparativo, certificação de distribuição ou
aceite de exportação pessoal. Relatórios/mídia privados não são publicados aqui.

## Pendências e próximo passo

1. Preservar os aceites focais já registrados de fonte/orientação/áudio/sync,
   prévia/faixas/histórico e alinhamento V1. Não repetir esses gates por reset.
2. Aceite pessoal final de salvar/reabrir/exportar/retomar na linha durável,
   nos destinos já designados. A ativação registrada não comprova aceite humano,
   nem garante que a sessão permaneça ativa hoje.
3. Recuperar fontes/evidências nos projetos atuais, conferir estado Git e seguir
   instruções detalhadas antes de executar. Não repetir leitura TAR ou testes
   aprovados sem mudança, falha nova ou preocupação concreta que o justifique.
4. Delimitar depois outros perfis, J-cuts, composição/legendas, áudio/cor/QA
   avançados, conversa/biblioteca duráveis, agentes/providers, distribuição e
   paridade EDvid completa. Nada disso está implementado por este contexto.

Integrações futuras preservam fontes originais, história própria de cada produto,
operações tipadas e aprovação explícita. Não há sincronização ou escrita automática
em outro app. Atualizações deste contexto devem conservar a distinção entre
implementado, comprovado por automação, aceito por humano e ainda pendente.

## Deltas locais consolidados — 09/11/2026

Fonte: índices locais e plano ativo de 19/10, reconferidos nos checkouts corretos.
Bases documentais: foundation `3964fa2`; durável `6c78a70`, com deltas locais
posteriores não publicados como código neste repositório.

- Linha ativa única: durável/exportação, preservando identidade e foundation como
  referência. Sem instalar pacote, criar outro clone ou fundir apps/stores.
- Aceites humanos focais acima registrados; porte durável de prévia limitada ao
  trecho, faixas permanentes e cartões V1 passou 20 verificações sintéticas e
  revisão independente. Isso não equivale a aceite pessoal de exportação.
- Exportação pessoal anterior falhou por SAR ausente. Foi implementada escolha
  explícita por fonte para declarar pixels quadrados, com histórico, Undo/Redo
  e checkpoint. Sem escolha, a recusa permanece; sinais conflitantes continuam
  recusados. Nenhuma declaração pessoal foi aplicada automaticamente.
- Reparo restrito do parser para terminador QuickTime válido passou sete testes
  focais. Retomada autorizada carregou o reparo, preservando checkpoint, histórico,
  cortes e falha anterior. Inspeção disponível não constitui exportação aprovada.
  Estado vivo da sessão não foi revalidado nesta consolidação.
- Três recortes offline registrados: catálogo de reuso, contexto compacto de
  transcript e SRT externo limitado a plano de cortes. Não representam ASR,
  composição completa, runtime pessoal integrado ou paridade funcional completa.
- Empacotamento/distribuição continuam pendentes. Próximo passo é o menor aceite
  humano ainda necessário, coordenado pelo usuário; sem renderização automática.

A publicação é somente documental e sanitizada. Não reexecuta testes de produto,
não inclui mídia, código, conversas ou caminhos pessoais. Revalidar por mudança
relevante, falha nova ou evidência incerta, não apenas por reset.
