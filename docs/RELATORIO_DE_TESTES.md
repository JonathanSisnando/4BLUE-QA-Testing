# Test Summary Report (TSR) - Projeto 4BLUE

## 1. Informações do Projeto e Ambiente
* **Responsável Técnico:** Jonathan Gabriel.
* **Versão do Produto:** 1.0.0[.
* **Plataforma:** WEB CMS ([https://qa-play-sim.lovable.app/](https://qa-play-sim.lovable.app/).
* **Data do Teste:** 06/03/2026: 4].
* **S.O. de Teste:** Windows 11.
* **Browser:** Google Chrome (Versão Estável).
* **Hardware:** Processador Intel(R) Core(TM) i7-9700 CPU @ 3.00GHz, 16,0 GB RAM.

## 2. Metodologia e Ferramentas
* **Método:** Caixa Preta].
* **Técnicas Aplicadas:** Partição de Equivalência, Análise de Valor Limite e Teste Baseado em Sessão (SBTM).
* **Evidências Dinâmicas (Vídeo):** Jam.
* **Evidências Estáticas (Screenshots):** LightShot.
* **Documentação Base:** Charter Exploratório (Excel/Markdown).

## 3. Métricas de Execução (KPIs)
Os indicadores abaixo refletem a saúde atual da aplicação testada com base na matriz de cobertura:

| Métrica | Valor | Percentual |
| :--- | :--- | :--- |
| **Total de Cenários Planejados** | 51 | 100% |
| **Cenários Executados com Sucesso (Pass)** | 31 | $\approx 60,78\%$ |
| **Cenários com Falha ou Melhoria (Issues)** | 26 | $\approx 39,22\%$ |

**Densidade de Defeitos:** Foi identificada uma concentração de $\approx 0,51$ defeitos por cenário, evidenciando instabilidade crítica nas validações de front-end.



[Image of software testing life cycle diagram]


---

## 4. Análise de Defeitos por Criticidade
| Categoria | Qtd | Prioridade de Correção | Impacto |
| :--- | :--- | :--- | :--- |
| **Crítico (Bloqueador)** | 2 | 1 - Imediata | Ruptura total da jornada do usuário. |
| **Segurança/Integridade** | 4 | 2 - Alta | Aceitação de dados inválidos e senhas frágeis. |
| **Usabilidade/UX** | 3 | 3 - Média | Erros de feedback e mensagens genéricas. |
| **Melhorias (Oportunidades)** | 17 | 4 - Baixa | Refinamento estético e Poka-Yoke. |

---

## 5. Respostas ao Desafio Técnico

### 5.1 Quais 2 bugs você corrigiria primeiro e por quê?

1.  **ID 0000028 - Sistema permite cadastro com senhas divergentes:**
    * **Justificativa:** É uma falha crítica de integridade. Permitir que o campo de confirmação divirja da senha original gera a criação de contas com credenciais inacessíveis, causando bloqueio imediato após o cadastro e perda de conversão do usuário.
2.  **ID 0000038 - Alerta "Conta não encontrada" para senha incorreta no Login:**
    * **Justificativa:** Prejudica a retenção e a segurança percebida. Ao informar que a conta não existe em vez de apontar erro de senha, o sistema induz o usuário a acreditar que seu cadastro foi perdido ou excluído, fragilizando a confiança na plataforma.

### 5.2 Sugestões de melhorias para as telas
Sugestões focadas em **Poka-Yoke** para mitigar riscos residuais:

* **Identificação Visual de Campos Inválidos:** Implementar sinalização imediata (bordas vermelhas `#ef4444`) nos campos de **E-mail** e **Senha** quando os dados inseridos forem inválidos. Atualmente, o sistema falha ao não fornecer feedback visual in-line antes da tentativa de submissão, deixando o usuário sem orientação clara sobre o erro cometido.
* **Trava de Ação (Submit):** Manter os botões de ação desabilitados (`disabled`) até que todas as regras de negócio e formatos de campo (Regex) sejam satisfeitos.
* **Sanitização Automática (Trim):** Implementar a remoção de espaços em branco automaticamente para evitar falhas de login por caracteres invisíveis.
* **Eliminação de Alertas Nativos:** Substituir `window.alert` por componentes de UI integrados (Toasts ou mensagens de erro abaixo dos inputs).

---

## 6. Parecer Final da Qualidade
**Status:** **NO-GO (Reprovado)**

[cite_start]**Fundamentação:** De acordo com os critérios de aprovação estabelecidos no Plano de Teste (Item 9.1), a liberação exige 0% de issues no fluxo principal[cite: 52]. Devido à presença de bugs críticos no módulo de autenticação, o sistema não atende aos requisitos mínimos para promoção ao ambiente de Produção.
