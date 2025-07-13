# 🎓 Sistema de Gestão de Cursos

Este repositório contém o **dicionário de dados** e estrutura básica de um sistema educacional que gerencia cursos, alunos, matrículas e suas respectivas aprovações.

---

## 🧾 Tabelas do Sistema

### 👨‍🎓 Tabela: `ALUNOS`
| Coluna      | Tipo        | Descrição             |
|-------------|-------------|------------------------|
| CPF         | CHAR(11)    | CPF do aluno (PK)      |
| DATA_NASC   | DATE        | Data de nascimento     |
| NOME        | VARCHAR(50) | Nome do aluno          |

---

### 📚 Tabela: `CURSOS`
| Coluna         | Tipo         | Descrição                    |
|----------------|--------------|-------------------------------|
| ID             | INT          | Identificador do curso (PK)  |
| VALOR          | DECIMAL      | Valor do curso               |
| CARGA_HORARIA  | INT          | Carga horária do curso       |
| N_TURMA        | VARCHAR(10)  | Número da turma              |
| DATA_DE_INICIO | DATE         | Início das aulas             |
| N_DE_VAGAS     | INT          | Número de vagas disponíveis  |

---

### 📝 Tabela: `MATRÍCULA`
| Coluna                 | Tipo     | Descrição                        |
|------------------------|----------|-----------------------------------|
| CÓDI_MATRI             | INT      | Código da matrícula (PK)          |
| DATA_DE_MATRÍCULA      | DATE     | Data da matrícula                 |
| NÚMERO_DE_PRESTAÇÕES   | INT      | Número de parcelas do pagamento   |

---

### ✅ Tabela: `APROVAÇÃO`
| Coluna       | Tipo     | Descrição                              |
|--------------|----------|-----------------------------------------|
| CPF_ALUNO    | CHAR(11) | CPF do aluno (FK de `ALUNOS`)           |
| NOTA         | DECIMAL  | Nota final no curso                     |
| SITUAÇÃO     | VARCHAR  | Status final (APROVADO / REPROVADO)     |
| N_MATRICULA  | INT      | Código da matrícula (FK de `MATRÍCULA`) |

---

## 🧠 Observações

- Relacionamento entre alunos e matrículas feito via CPF.
- Situação da aprovação depende da nota.
- O sistema está preparado para múltiplos cursos e turmas simultâneos.

---

## 💡 Possíveis Extensões

- Tabela para professores e disciplinas.
- Histórico acadêmico completo.
- Emissão de certificados automáticos.

---

## 📄 Licença

Projeto livre para fins acadêmicos. Licenciado sob a [MIT License](LICENSE).

---

## ✨ Contribua!

Pull requests são bem-vindos! Abra uma *issue* para sugerir melhorias ou reportar bugs.

---
