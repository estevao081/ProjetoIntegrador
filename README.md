# Projeto Integrador

## Protótipo no Figma
👉 [Acessar protótipo interativo](https://www.figma.com/make/cp6MPL4s5limQDyXA4KIBI/User-Dashboard?node-id=0-1&p=f&fullscreen=1)

---

## Descrição
O **Projeto Integrador** tem como objetivo a construção de um sistema acadêmico unificado que permita o gerenciamento de **alunos**, **professores**, **fornecedores** e **departamentos**.  
O sistema visa integrar os principais processos administrativos e acadêmicos em um único ambiente, oferecendo funcionalidades como **solicitação de histórico**, **alocação de disciplinas**, **cadastro de pessoas físicas e jurídicas**, e **solicitação de cotações**.

---

## Objetivos do Sistema
- Centralizar os cadastros de pessoas físicas e jurídicas.  
- Automatizar processos administrativos, como alocação de professores e solicitação de cotações.  
- Facilitar a gestão acadêmica e institucional de forma integrada.  
- Promover a reutilização e especialização de classes, aplicando **princípios de POO** e **UML**.

---

## Atores do Sistema
- **Aluno:** pode solicitar histórico acadêmico.  
- **Professor:** pode ser alocado em disciplinas e vinculado a um departamento.  
- **Administrador/Secretaria:** responsável por cadastros e controle de entidades.  

---

## Casos de Uso Principais
| Ator | Caso de Uso | Descrição |
|------|--------------|-----------|
| Aluno | Solicitar Histórico | Permite ao aluno visualizar seu histórico acadêmico. |
| Professor | Alocar Disciplina | Permite ao professor ser alocado em uma disciplina. |
| Administrador/Secretaria | Cadastro de Aluno | Cadastra um novo aluno, estendendo o cadastro de pessoa física. |
| Administrador/Secretaria | Cadastro de Professor | Cadastra um professor, também como pessoa física. |
| Administrador/Secretaria | Cadastro de Fornecedor | Registra um fornecedor, estendendo o cadastro de pessoa jurídica. |
| Administrador/Secretaria | Solicitar Cotação | Solicita uma cotação a um fornecedor cadastrado. |

---

## Diagrama de Caso de Uso
![Diagrama de caso de uso](imgs/Diagrama%20de%20caso%20de%20uso.png)

---

## Diagrama de Classes
![Diagrama de Classes](imgs/Diagrama%20de%20classes.jpg)

---

## Estrutura de Classes

### Classe `Pessoa`
Classe base para todas as entidades relacionadas a pessoas.

| Atributo | Tipo | Descrição |
|-----------|------|-----------|
| id | Long | Identificador único |
| nome | String | Nome completo |
| endereco | String | Endereço da pessoa |
| telefone | String | Contato telefônico |

**Métodos:**
- `salvar()`
- `consultar()`

---

### Subclasses de Pessoa
#### Pessoa Física
- **cpf:** String  
- **dataNascimento:** LocalDate  

#### Pessoa Jurídica
- **cnpj:** String  
- **razaoSocial:** String  
- **nomeFantasia:** String  

---

### Entidades Derivadas

#### Aluno
- **matricula:** String  
- **dataIngresso:** LocalDate  
- **endereco, telefone** (herdados)  
- **Método:** `solicitarHistorico()`

#### Professor
- **titulacao:** String  
- **materia:** String  
- **Método:** `alocarDisciplina()`

#### Fornecedor
- **categoria:** String  
- **inscricaoEstadual:** String  
- **contatoComercial:** String  
- **Método:** `solicitarCotacao()`

#### Departamento
- **id:** Long  
- **nome:** String  
- **sigla:** String  
- **Método:** `adicionarProfessor()`

**Relacionamento:**  
Um departamento pode ter **vários professores** (*1:N*).

---

## Tecnologias Envolvidas
- **Figma** – modelagem visual dos diagramas  
- **UML** – documentação e padronização da modelagem  

---

## Autores
**Thiago Estevão**  
**Nicolas Soares**  
**Lara Ferreira Gonçalves**  
**Gabriela Sarto**


---

Projeto desenvolvido como parte do **Projeto Integrador**, com foco em **modelagem UML e POO aplicada a sistemas acadêmicos**.
