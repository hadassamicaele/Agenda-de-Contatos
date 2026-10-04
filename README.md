Markdown
# 📱 Agenda de Contatos

> Sistema de gerenciamento de contatos desenvolvido em **Java** para a disciplina de **Programação Orientada a Objetos (POO)**.

O projeto consiste em uma aplicação de agenda de contatos que evolui incrementalmente a cada versão, aplicando conceitos fundamentais de programação, estruturas de dados, modularização e persistência de informações.

---

## 🎯 Objetivo

Desenvolver um sistema de Agenda de Contatos em Java, colocando em prática os principais conceitos de programação, como:

- 🧩 Programação Orientada a Objetos
- 📦 Organização e separação de classes
- 🔄 Estruturas de repetição e condicionais
- 📚 Coleções dinâmicas (`ArrayList`)
- 🖥️ Interfaces gráficas com `JOptionPane`
- 💾 Persistência de dados em arquivos de texto
- 🛠️ Operações CRUD (Create, Read, Update, Delete)

---

## 📈 Evolução do Projeto

O sistema foi desenvolvido em etapas, com novas funcionalidades e melhorias estruturais adicionadas a cada versão.

| Versão | Estrutura | Principais conceitos |
|:---:|---|---|
| `V.0.0.0` | Variáveis simples | `Scanner`, condicionais, `switch` e `while` |
| `V.0.1.0` | Vetores | Matrizes, índices, `for` e capacidade fixa |
| `V.0.2.0` | `ArrayList` | Coleções dinâmicas, `add()`, `get()`, `remove()` e `size()` |
| `V.0.3.0` | `ArrayList` | Atualização com `set()` e implementação do CRUD |
| `V.1.0.0` | Modularização | Organização do código em métodos estáticos |
| `V.1.1.0` | Separação em classes | Classes `Principal`, `Agenda` e `Uteis`, com `JOptionPane` |
| `V.1.1.1` | Correção de fluxo | Método `sair()` com retorno `boolean` e controle do `do-while` |
| `V.2.1.0` | Persistência em arquivo | Salvamento e carregamento automático com arquivos `.txt` |

---

## 🚀 Versão Atual — V.2.1.0

A versão **V.2.1.0** introduz a persistência de dados em arquivo de texto, permitindo que os contatos cadastrados permaneçam salvos mesmo após o encerramento da aplicação.

### 💾 Persistência de Dados

A nova classe `Persistencia.java` é responsável pelo armazenamento e pela recuperação das informações.

- 📥 **`carregarContatos()`**  
  Lê os dados do arquivo `contatos.txt` utilizando `BufferedReader` e `FileReader`, reconstruindo as listas de contatos na memória. Também trata arquivos inexistentes e registros malformados.

- 📤 **`salvarContatos()`**  
  Grava os contatos no arquivo `contatos.txt`, utilizando `FileWriter` e `PrintWriter`, com os campos separados por ponto e vírgula (`;`).

### 🔄 Integração com o Sistema

- Carregamento automático dos contatos ao iniciar o programa.
- Salvamento dos dados ao selecionar a opção **6 — Sair**.
- Preservação das informações cadastradas entre as execuções.

---

## ⚙️ Funcionalidades

| Ícone | Funcionalidade | Descrição |
|:---:|---|---|
| ➕ | **Adicionar contato** | Cadastra nome, celular e e-mail. |
| 📋 | **Listar contatos** | Exibe todos os contatos cadastrados. |
| 🔎 | **Procurar contato** | Busca um contato específico pelo nome. |
| ✏️ | **Alterar contato** | Atualiza as informações de um contato existente. |
| 🗑️ | **Excluir contato** | Remove um contato da agenda. |
| 🚪 | **Sair** | Salva os dados em `contatos.txt` e encerra o programa. |
| ℹ️ | **Sobre** | Exibe informações do desenvolvedor por meio de `JOptionPane`. |

---

## 🛠️ Tecnologias Utilizadas

- ☕ **Java** — Linguagem de programação.
- 🖥️ **JOptionPane** — Exibição de janelas gráficas.
- 📚 **ArrayList** — Armazenamento dinâmico dos contatos.
- 📄 **FileWriter / PrintWriter** — Gravação de dados em arquivos.
- 📖 **FileReader / BufferedReader** — Leitura de arquivos.
- 🌿 **Git e GitHub** — Controle de versão e hospedagem do código.

---

## 📂 Estrutura do Projeto

```text
Agenda-Contatos/
│
├── .gitignore
├── README.md
├── contatos.txt
│
└── src/
    └── br/
        └── edu/
            └── principal/
                ├── Agenda.java
                ├── Persistencia.java
                ├── Principal.java
                └── Uteis.java
