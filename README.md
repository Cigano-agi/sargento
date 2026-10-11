# SARGENTO v1.1 — Consultor de Debug & Refatoração

> "Eu não conserto código. Eu conserto engenheiros." — @cigano.agi

---

## O que é

O **SARGENTO** é um agente de debug e refatoração com protocolo de 4 fases, baseado em pesquisa acadêmica real. Funciona como um engenheiro sênior com 30+ anos de experiência que faz diagnóstico cirúrgico do seu projeto — não tapa buracos, resolve a causa raiz.

Criado por **Bruno Fabricio Feitosa** ([@cigano.agi](https://instagram.com/cigano.agi)).

---

## Protocolo de 4 Fases

| Fase | Nome | O que faz |
|------|------|-----------|
| FASE 0 | INTAKE | Interrogatório estruturado: até 48 perguntas em 8 blocos |
| FASE 1 | COMPREENSÃO | Mapeia escopo, fluxo de dados, invariantes e code smells |
| FASE 2 | NAVEGAÇÃO | Localiza falhas, analisa propagação, classifica severidade |
| FASE 3 | CONFIRMAÇÃO E CORREÇÃO | Patches com diff, validação e plano de execução |
| FASE 4 | CONSOLIDAÇÃO | Documentação, recomendações estruturais, transferência de conhecimento |

---

## Plataformas Suportadas

| Plataforma | Integração | Documentação |
|---|---|---|
| **Claude Code** | Agente local (`~/.claude/agents/sargento.md`) | [Ver instruções](#como-instalar-no-claude-code) |
| **Google Antigravity** | Agente autônomo & Subagente PoP-M2M | [Guia Antigravity](integrations/antigravity/README.md) |

---

## Como instalar no Claude Code

### Opção 1 — Agente local (recomendado)

```bash
# Clone o repo
git clone https://github.com/Cigano-agi/sargento.git

# Copie para a pasta de agentes do Claude Code
cp sargento/sargento.md ~/.claude/agents/sargento.md
```

Reinicie o Claude Code. O Sargento aparece automaticamente como agente.

### Opção 2 — Copiar manualmente

1. Baixe [sargento.md](./sargento.md)
2. Coloque em:
   - Mac/Linux: `~/.claude/agents/sargento.md`
   - Windows: `%USERPROFILE%\.claude\agents\sargento.md`
3. Reinicie o Claude Code

### Opção 3 — Usar direto

Copie o conteúdo de `sargento.md` e cole como system prompt em qualquer LLM.

---

## Fundamentos acadêmicos

- **Mei et al. (2025)** — Survey de Context Engineering (arXiv:2507.13334)
- **Qin et al. (2024)** — AgentFL: multi-agente compreensão → navegação → confirmação (arXiv:2403.16362)
- **DEVLoRe (2024)** — +60.2% bugs corrigidos com multi-artifact context (arXiv:2412.03905)
- **Badampudi et al. (2023)** — Modern Code Reviews (ACM TOSEM)

---

## Criador

**Bruno Fabricio Feitosa** — Builder, estrategista de IA, fundador da Gypsi Ventures.

- Instagram: [@cigano.agi](https://instagram.com/cigano.agi)
- Comunidade gratuita: [A Guilda](https://instagram.com/cigano.agi)

---

## Licença

MIT — use, adapte, redistribua.

```
@cigano.agi — me segue lá, recruta.
```
