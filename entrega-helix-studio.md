# ENTREGA — BRIEF HELIX STUDIO
> Prompt Engineering para Desenvolvedores · tarefa realizada com agente de IA

## 1. Identificação
- Aluno(a): — (preencher)
- Turma: — (preencher)
- Data: 05/10/2026

## 2. Links do produto
- Repositório (GitHub): — (pendente: ainda não publicado)
- Site publicado: — (pendente: ainda não publicado)

## 3. Requisitos da cliente
- [x] R1 — One-page responsiva em HTML + CSS + JS
- [x] R2 — Seções: hero, recursos (mín. 3), demonstração, contato
- [x] R3 — Demo funcional: notas salvando no localStorage (criar, listar, excluir)
- [x] R4 — Textos reais e coerentes — zero lorem ipsum
- [x] R5 — Zero erros no console do navegador
- [ ] R6 — No ar: GitHub + Vercel/Netlify com URL funcionando (pendente: depende da conta do aluno)

Como R1 a R5 foram verificados: teste automatizado em Chromium headless (Playwright). Cobriu criar, listar, excluir com desfazer, busca, persistência após recarregar, rascunho, bloco de código, texto HTML tratado como texto (sem XSS), console limpo em desktop (1280px) e em celular (375px), e ausência de rolagem horizontal em 375px. Verificação estática: nenhum "lorem", nenhum `alert()`, 4 recursos, tags HTML balanceadas.

## 4. Etapas do roteiro
O roteiro sugerido (P0–P7, um objetivo por prompt, com teste entre cada etapa) NÃO foi seguido ciclo a ciclo: o site foi construído em uma única passada, a partir de uma análise prévia dos dois arquivos HTML da atividade. As etapas abaixo refletem o que existe no resultado, não o processo prescrito.
- [ ] P0 — Plano antes do código (não houve aprovação de plano separada)
- [ ] P1 — Estrutura + hero (entregue junto, em um único prompt)
- [ ] P2 — Recursos (entregue junto)
- [ ] P3 — Demo funcional (entregue junto)
- [ ] P4 — Contato + textos (entregue junto)
- [ ] P5 — Responsivo (testado em 375px por automação, não em celular real)
- [ ] P6 — Revisão de qualidade (feita pelo próprio agente via testes; ver diário #2)
- [x] P7 — README + preparação do deploy (README.md criado)

## 5. Publicação
- [ ] G1 — Repositório PÚBLICO criado no GitHub
- [ ] G2 — Arquivos enviados (commit + push)
- [x] G3 — README.md com nome do projeto e como visualizar (arquivo pronto, falta commitar)
- [ ] D1 — Projeto importado da Vercel OU Netlify a partir do GitHub
- [ ] D2 — Deploy concluído — a URL abre o site sem erro
- [ ] D3 — Testado no celular (responsivo de verdade)

## 6. Diário de prompts (2 registros)

### #1 — Analisar os dois HTML da atividade — FUNCIONOU DIRETO
PROMPT ENVIADO:
"""
Você é um engenheiro de Software senior. Analise esses html.
"""
RESPOSTA DO AGENTE:
"""
Leitura completa dos dois arquivos e execução do motor heurístico do simulador em Node. Entregou análise com pontos fortes e problemas por prioridade, entre eles: simulador enganável por palavras-chave (100/100) e falso positivo em "Não explique"; exemplos fortes dos cenários 02 e 03 abaixo de 80 pontos; promessa de "100% local" contradita por unpkg@latest e Google Fonts; acessibilidade ausente (zero aria, focus-visible e reduced-motion); e e-mail da cliente sem quebra de linha no brief.
"""

### #2 — Executar a atividade a partir da análise — FUNCIONOU APÓS AJUSTE
PROMPT ENVIADO:
"""
usando essa análise como base e os html, faça a atividade
"""
RESPOSTA DO AGENTE:
"""
Construiu o site de uma página (index.html, sem dependências externas) e o README, e testou com navegador headless. Ajustes feitos durante a própria execução: conflito de CSS entre a barra do topo e a grade do hero; colunas de grid que vazavam em 375px (corrigido com minmax(0,1fr)); placeholder cortado; nota sem título mostrando crases na mini-lista. Decisões herdadas da análise: sem fontes/scripts de terceiros (tudo local, coerente com a promessa de "no seu navegador"), skip link, rótulos em todos os campos, foco visível, prefers-reduced-motion, mensagens de erro sem alert(), blocos de código inseridos via textContent.
"""

## 7. Observações
- O brief pede 5 a 8 registros no diário e que o aluno DIRIJA o agente em vários ciclos e consiga explicar qualquer trecho do código. Este diário tem só os 2 prompts que realmente ocorreram. Os demais registros devem ser do próprio aluno, em interações reais, sem inventar entradas.
- Pendências para fechar o contrato: preencher nome e turma, criar o repositório, publicar na Vercel/Netlify, testar em celular real e colar os dois links.
- Os links de redes sociais da seção de contato apontam para a página inicial de cada rede e o e-mail usa o domínio fictício .example; trocar pelos dados reais da Helix Studio antes de divulgar.

---
_Declaração: ainda NÃO posso declarar que o site está no ar. Falta o deploy._
