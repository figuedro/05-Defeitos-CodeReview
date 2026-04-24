# 📦 Relatório Final

> **Atividade:** Bug Report Profissional + Code Review Guiado
> **Curso:** Qualidade de Software
> **Professor:** Prof. Claudio Nunes

---

## 👥 Identificação da dupla

| Nome completo | RA | GitHub |
|---|---|---|
| [João Pedro Unger Dias Figueiredo] | [226793] | [@figuedro] |
| [Matheus Cardoso Martins] | [228828] | [@MatheusCardoso013] |

**Ambiente de testes:** [Descreva brevemente o setup — Chrome Versão 140.0.7339.186 no Windows 10 (Versão 22H2), GitHub Pages do fork, Visual Studio Code]

---

## 📋 Sumário

- [Parte A — Bug Reports](#parte-a--bug-reports)
- [Parte B — Code Review](#parte-b--code-review)
- [Reflexão final](#-reflexão-final)
- [Declarações](#-declarações)

---

## Parte A — Bug Reports

# 🐛 Bug Reports — Parte A

**Dupla:** [João Pedro Unger Dias Figueiredo + 226793] + [Matheus Cardoso Martins + 228828]
**Data da exploração:** [23/04/2026]
**Navegador usado:** [Chrome 140.0.7339.186]
**Sistema operacional:** [Windows 10]

---

## BUG-001

**Título:** [CONTEXTO] Ao clicar no botão de Limpar campos, o sistema remove o valor apenas dos campos Título, Categoria e Prazo, Prioridade mantem o valor antigo.

**Severidade:** Média
**Justificativa da severidade:** Usuário pode querer cadastrar outra tarefa e acabar não percebendo que o campo manteve o valor, ou até mesmo editar uma tarefa em que estava cadastrando e o valor antigo ficar.

**Prioridade:** P2
**Justificativa da prioridade:** Usuários podem acabar cadastrando tarefas de forma errada, e se confundirem com suas prioridades

**Ambiente:**
- Navegador: [Chrome 140.0.7339.186]
- Sistema Operacional: [Windows 10]
- Versão da aplicação: TarefaQS v1.0.0

**Passos para reprodução:**
1. Preencher campos para cadastro de uma tarefa
2. Após os campos terem valores preenchidos, clicar no botão **Limpar campos**
3. Verificar que os campo Prioridade manteve valor digitado no Passo 1

**Resultado esperado:**
[Todos os campos deveriam ter os valores limpos]

**Resultado obtido:**
[Apenas tres campos tem o valor removido, porém o campo Prioridade mantem o valor]

**Evidência:**
![Descrição da evidência]

<img width="788" height="288" alt="cadastro-apos-limpar-campos" src="https://github.com/user-attachments/assets/93cd4929-24d0-4a51-ac31-c73471555bb9" />
<img width="801" height="294" alt="cadastro-tarefa" src="https://github.com/user-attachments/assets/d27fe16b-ce04-4388-8d82-31b245e34ad6" />


**Sugestão de causa raiz (opcional):**
[Provavelmente o botão não deve chamar o campo para ser limpo]

---

## BUG-002

**Título:** [CONTEXTO] Ao inserir um valor no campo Prioridade, o sistema permite eu cadastrar com qualquer valor numerico.

**Severidade:** Baixa
**Justificativa da severidade:** Usuário pode acabar colocando um valor fora do escopo, porem não impacta diretamente o uso da aplicação.

**Prioridade:** P3
**Justificativa da prioridade:** Usuários podem acabar cadastrando tarefas de forma errada, e se confundirem com suas prioridades

**Ambiente:**
- Navegador: [Chrome 140.0.7339.186]
- Sistema Operacional: [Windows 10]
- Versão da aplicação: TarefaQS v1.0.0

**Passos para reprodução:**
1. Preencher campos para cadastro de uma tarefa, e colocar valor fora do escopo no campo Prioridade
2. Após os campos terem valores preenchidos, clicar no botão **Adicionar tarefa**
3. Verificar nas tarefas cadastradas que o campo prioridade sai do escopo definido pela aplicação 1-5

**Resultado esperado:**
[Campos prioridade devia ser limitado ao valor de 1-5]

**Resultado obtido:**
[Qualquer valor numerico pode ser adicionado]

**Evidência:**
![Descrição da evidência]





**Sugestão de causa raiz (opcional):**
[O campo prioridade não possui algum tipo de validação para garantir que o valor esteja entre 1 e 5]

---

## BUG-003

**Título:** [CONTEXTO] Ao clicar no botão Adicionar tarefa, é possivel cadastrar tarefas sem preencher os campos, criando uma tarefa vazia.

**Severidade:** Alta
**Justificativa da severidade:** Usuários podem cadastrar tarefas infinitas e sobrecarregar o sistema.

**Prioridade:** P1
**Justificativa da prioridade:** Usuários podem cadastrar inumeras tarefas sem valores

**Ambiente:**
- Navegador: [Chrome 140.0.7339.186]
- Sistema Operacional: [Windows 10]
- Versão da aplicação: TarefaQS v1.0.0

**Passos para reprodução:**
1. Clicar no botão **Adicionar tarefa** sem preencher nenhum dado
2. Verificar nas tarefas cadastradas que foi cadastrada uma tarefa sem nenhum dado incluso

**Resultado esperado:**
[Para criar uma tarefa os valores devem ter valores preenchidos]

**Resultado obtido:**
[É possivel cadastrar tarefas sem valores]

**Evidência:**
![Descrição da evidência]

> Se preferir anexar um GIF ou arquivo de log, crie uma pasta
> `evidencias/` ao lado deste arquivo e referencie o arquivo aqui.

**Sugestão de causa raiz (opcional):**
[O campo prioridade não possui algum tipo de validação para garantir que o valor esteja entre 1 e 5]

---

## ✅ Critérios de qualidade do bug report
*(Use para conferir antes de entregar)*

- [x] Título descritivo — outra pessoa entende o problema só pelo título?
- [x] Passos são **numerados** e **reproduzíveis** por terceiros?
- [x] Há **pelo menos uma evidência** (screenshot, GIF ou log)?
- [x] Severidade tem **justificativa explícita**?
- [x] Prioridade tem **justificativa explícita**?
- [x] Ambiente inclui **navegador + SO**?
- [x] "Esperado vs. Obtido" deixa o gap claro?

## ✅ Checklist de qualidade dos reports

Antes de submeter, confirme em cada report:

- [x] Título é específico e acionável (não `"Não funciona"`).
- [x] Passos estão **numerados** e são reproduzíveis por terceiros.
- [x] Há **pelo menos uma evidência** por report (imagem, GIF ou log).
- [x] Severidade tem **justificativa explícita**.
- [x] Prioridade tem **justificativa explícita**.
- [x] Ambiente inclui **navegador + SO**.
- [x] "Esperado × Obtido" deixa a diferença clara.
- [x] Os 3 defeitos reportados cobrem **categorias diferentes**
      (funcional, UX, validação, persistência, etc.)

---

## Parte B — Code Review

### Resumo

# | Linha    | Dimensão         | Rótulo                         | Severidade
--|----------|------------------|--------------------------------|------------
1 | 5        | Manutenibilidade | Constante não utilizada        | Baixa
2 | 10–13    | Confiabilidade   | Não tratar erros               | Média
3 | 12       | Segurança        | SQL Injection                  | Crítica
4 | 20–35    | Segurança        | Falta de validação de dados    | Alta
5 | 112–150  | Manutenibilidade | Código duplicado               | Média
6 | 37–43    | Legibilidade     | Nomes pouco descritivos        | Baixa

### Findings detalhadas

# 🔎 Formulário — Parte B

> Preencha uma seção por finding. O mínimo esperado é **6 findings**.

**Dupla:** [João Pedro Unger Dias Figueiredo + 226793] + [Matheus Cardoso Martins + 228828]
**Data da revisão:** [23/04/2026]

---

### Finding #1

**📍 Linha(s):*5*
**🏷 Rótulo:** Constante não utilizada para validação
**📂 Dimensão:** Manutenibilidade
**⚠️ Severidade:** Baixa

**🐛 Problema:**
A constante TIPOS_VALIDOS é declarada, mas não é utilizada em nenhum ponto do código para validar o tipo de usuário.

**💡 Sugestão de correção:**


```javascript
async function cadastrarUsuario(dados) {
  if (!TIPOS_VALIDOS.includes(dados.tipo)) {
    throw new Error('Tipo de usuário inválido');
  }

  const salt = 10;
  const senhaHash = await crypto.hash(dados.senha, salt);

  const usuario = {
    nome: dados.nome,
    email: dados.email,
    tipo: dados.tipo,
    senha: senhaHash,
    ativo: true,
    criadoEm: new Date().toISOString()
  };

  await db.insert('usuarios', usuario);
  return usuario;
}
```

**📚 Referência (opcional):**

---

### Finding #2

**📍 Linha(s):*10-13*
**🏷 Rótulo:*Não tratar erros*
**📂 Dimensão:*Confiabilidade*
**⚠️ Severidade:*Média*

**🐛 Problema:**
Chamadas assíncronas ao banco não possuem tratamento de erro.
**💡 Sugestão de correção:**

```javascript
async function listarUsuariosAtivos() {
  try {
    return await db.executarQuery('SELECT * FROM usuarios WHERE ativo = 1');
  } catch (err) {
    logger.error('Erro ao listar usuários ativos', err);
    throw err;
  }
}
```

---

### Finding #3

**📍 Linha(s):*12*
**🏷 Rótulo:** Sql Injection
**📂 Dimensão:** Segurança
**⚠️ Severidade:** Crítica

**🐛 Problema:**
A query SQL possui uma concatenacao, ou seja se o Usuario inserir um valor que interfira no SQL a query pode ser executada com o valor digitado pelo usuario

**💡 Sugestão de correção:**
Usar queries parametrizadas

```javascript
const query = "SELECT * FROM usuarios WHERE nome = ?";
connection.execute(query, [nome], (err, results) => {
  // tratar resultado
});
```

**📚 Referência (opcional):**

---

### Finding #4

**📍 Linha(s):*20-35*
**🏷 Rótulo:*Falta de validação de dados*
**📂 Dimensão:*Segurança*
**⚠️ Severidade:*Alta*

**🐛 Problema:**
Os dados de entrada (dados.nome, dados.email, dados.tipo, dados.senha) não são validados antes de serem usados.

**💡 Sugestão de correção:**

```javascript
if (!dados.nome || !dados.email || !dados.senha) {
  throw new Error('Dados obrigatórios não informados');
}

if (!TIPOS_VALIDOS.includes(dados.tipo)) {
  throw new Error('Tipo de usuário inválido');
}
```

---

### Finding #5

**📍 Linha(s):*112–150*
**🏷 Rótulo:*Código duplicado*
**📂 Dimensão:*Manutenibilidade*
**⚠️ Severidade:*Media*

**🐛 Problema:**
Lógica duplicada entre calcularLimiteEmprestimo e calcularLimiteComSuspensao..

**💡 Sugestão de correção:**

```javascript
function calcularLimiteBase(usuario) {
  // regras aqui
}

function calcularLimiteComSuspensao(usuario) {
  if (usuario.suspenso) return 0;
  return calcularLimiteBase(usuario);
}
```

---

### Finding #6

**📍 Linha(s):*37–43*
**🏷 Rótulo:*Nomes pouco descritivos*
**📂 Dimensão:*Legibilidade*
**⚠️ Severidade:*Baixa*

**🐛 Problema:**
Uso de variáveis genéricas como u, dificultando entendimento.

**💡 Sugestão de correção:**

```javascript
const usuario = await db.buscarPorId('usuarios', id);
```

---

---

## ✅ Checklist final

- [x] Há pelo menos 6 findings preenchidas
- [x] Cada finding cita linha, dimensão, rótulo e severidade
- [x] As sugestões são concretas e acionáveis
- [x] Pelo menos uma finding cobre segurança
- [x] Pelo menos uma finding cobre complexidade

---

## 💭 Reflexão final

> Responda em 1-2 parágrafos. Esta reflexão **é obrigatória**.

**Qual dimensão do checklist foi mais difícil aplicar? Por quê?**

Relatar os erros e suas descrições, categorizar o nivel de severidade e prioridade, e descrever com clareza para qualquer um poder entender os erros presentes e reproduzir

**O que vocês fariam diferente se revisassem o código novamente?**

Usaria o checklist com mais frequencia, ele ajuda a identificar melhor os erros e não se perder no caminho

---

## 📣 Declarações


### Uso de IA como parceiro de trabalho

- [ ] Não usamos IA nesta atividade.
- [ ] Usamos IA para esclarecer conceitos teóricos.
- [ ] Usamos IA para revisar a redação dos bug reports.
- [ ] Usamos IA para discutir se um achado era ou não um defeito.
- [x] Uso específico: [Usei a Ia para recomendar ajustes no código javascript]

### Declaração de autoria

Declaramos que este relatório é de autoria da dupla, que exploramos
pessoalmente a aplicação da Parte A e lemos o código da Parte B. As
findings aqui registradas representam nosso próprio julgamento
técnico.
