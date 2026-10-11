# SARGENTO — Guia de Instalação e Uso no Google Antigravity

Bem-vindo à integração oficial do **SARGENTO** para o **Google Antigravity**.

O SARGENTO é uma consultoria sênior de debug e refatoração com 30+ anos de experiência mental em sistemas críticos, criado por [@cigano.agi](https://github.com/Cigano-agi). Este módulo expande o alcance do Sargento para o ecossistema Google Antigravity, permitindo operação tanto como **agente autônomo** quanto como **subagente tático PoP-M2M** (Protocol of Protocols / Machine-to-Machine).

---

## 🚀 Capacidades no Google Antigravity

- **Inspeção Cirúrgica (`view_file`):** Leitura de trechos com `StartLine` e `EndLine`, prevenindo saturação de contexto (*Context Rot*).
- **Edição Atômica (`replace_file_content`):** Aplicação de patches cirúrgicos linha a linha sem corromper arquivos com regravações integrais desnecessárias.
- **Execução Real de Linters e Testes (`run_command`):** Totalmente adaptado para PowerShell no Windows e Bash em Linux/macOS.
- **Topologia Híbrida PoP-M2M (`send_message`):** Pode operar como subagente especialista recebendo ordens operacionais de um coordenador e devolvendo relatórios táticos sintéticos.

---

## 📦 Métodos de Instalação

### Método 1: No Workspace Atual (Recomendado por Projeto)

Para disponibilizar o Sargento em um repositório específico sob o Antigravity:

1. Na raiz do seu projeto, crie a pasta de regras do agente:
   ```bash
   mkdir -p .agent/rules
   ```
2. Copie a definição do Sargento para o diretório de regras:
   ```bash
   cp integrations/antigravity/sargento.md .agent/rules/sargento.md
   ```
3. O Google Antigravity carregará as diretrizes automaticamente em todas as sessões dentro do workspace.

---

### Método 2: Instalação Global no Perfil de Agente (Antigravity CLI / Global)

Para ter o Sargento disponível em qualquer workspace da sua máquina:

#### No Windows (PowerShell):
```powershell
New-Item -ItemType Directory -Force -Path "$HOME\.gemini\antigravity\personas"
Copy-Item "integrations\antigravity\sargento.md" -Destination "$HOME\.gemini\antigravity\personas\sargento.md"
```

#### No Linux / macOS:
```bash
mkdir -p ~/.gemini/antigravity/personas
cp integrations/antigravity/sargento.md ~/.gemini/antigravity/personas/sargento.md
```

Após copiar, você pode referenciar o Sargento nas instruções customizadas da IDE ou via CLI com a flag de persona/instrução de sistema.

---

### Método 3: Operação como Subagente em Topologias PoP-M2M

Se você utiliza sistemas multiagentes coordenados (ex: Arquiteto, Comandante ou Agente Primário orquestrando subagentes especialistas), registre o Sargento como a unidade tática de **Debug & Refatoração**:

```json
{
  "subagents": {
    "sargento": {
      "role": "Debug & Refactoring Senior Consultant",
      "instruction_file": "integrations/antigravity/sargento.md",
      "capabilities": ["code_audit", "root_cause_analysis", "atomic_patching", "test_verification"]
    }
  }
}
```

Quando acionado pelo agente orquestrador via `send_message`, o Sargento responde no formato M2M sintético com os patches cirúrgicos e a tese de causa raiz validada.

---

## 🎯 Exemplos de Invocação

### 1. Incidente Crítico ("Tá tudo quebrado")
> *"Sargento, subimos o deploy para staging e os workers pararam de processar a fila. Tá tudo quebrado. Execute o protocolo completo."*

O Sargento abrirá o interrogatório das 8 fases, isolará o blast radius e aplicará a correção cirúrgica.

### 2. Refatoração Cirúrgica
> *"Sargento, este serviço de pagamento tem 800 linhas e alta complexidade ciclomática. Mapeie os code smells e aplique a refatoração sem quebrar os testes."*

O Sargento mapeará invariantes, catalogará smells e aplicará patches atômicos com `replace_file_content`.

### 3. Chamada Machine-to-Machine (PoP-M2M)
```text
[ORDEM OPERACIONAL PoP-M2M]
[ALVO]: src/services/auth.ts
[AÇÃO]: Diagnóstico de race condition no refresh token e patch corretivo.
```

---

## ⚖️ Claude Code vs. Google Antigravity

| Recurso | Claude Code | Google Antigravity |
| :--- | :--- | :--- |
| **Ponto de Entrada** | Slash Command (`/sargento`) | Regra de Workspace / Persona Global / Subagente M2M |
| **Ferramenta de Edição**| Edit / Patch nativo | `replace_file_content` (atômico e seguro) |
| **Ambiente de Terminal**| Shell Unix nativo | PowerShell (Windows) + Bash (Linux/macOS) |
| **Modo Multiagente** | Interativo único | Híbrido: Chat direto ou Subagente via `send_message` |
| **Fundamentos** | Mei et al. / AgentFL / DEVLoRe | Idênticos — 100% preservados |

---

## 📜 Licença e Créditos

- **Criador:** [@cigano.agi](https://github.com/Cigano-agi)
- **Repositório Oficial:** [github.com/Cigano-agi/sargento](https://github.com/Cigano-agi/sargento)
- **Filosofia:** *Causa raiz > sintoma. Remendo sobre remendo é suicídio técnico.*
