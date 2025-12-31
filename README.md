# 🗄️ Diagramas EER - Modelagem de Banco de Dados

[![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=for-the-badge&logo=mysql&logoColor=white)](https://www.mysql.com/)
[![Oracle](https://img.shields.io/badge/Oracle_Data_Modeler-F80000?style=for-the-badge&logo=oracle&logoColor=white)](https://www.oracle.com/database/sqldeveloper/)
[![Database](https://img.shields.io/badge/Database_Design-Expert-success?style=for-the-badge)]()

> **Portfólio de modelagem de banco de dados relacional**  
> Coleção de diagramas EER desenvolvidos para demonstração de competências em modelagem de dados

Repositório com 5 diagramas EER (Enhanced Entity-Relationship) completos, abrangendo diferentes domínios de negócio e níveis de complexidade. Desenvolvidos com MySQL e Oracle Data Modeler como parte da formação técnica em Ciência de Dados.

---

## 📖 Sobre o Projeto

Este portfólio demonstra **competências práticas em modelagem de banco de dados**, incluindo:

✅ **Análise de requisitos** - Tradução de regras de negócio em estruturas de dados  
✅ **Normalização** - Aplicação de formas normais (1FN a 3FN)  
✅ **Relacionamentos complexos** - Cardinalidades 1:1, 1:N, N:M  
✅ **Integridade referencial** - Chaves primárias e estrangeiras  
✅ **Modelagem conceitual e lógica** - Do conceito à implementação  

---

## 🗂️ Diagramas Desenvolvidos

### 📊 Visão Geral

| # | Diagrama | Domínio | Entidades | Complexidade |
|---|----------|---------|-----------|--------------|
| 1️⃣ | DbProjetos_Aram | Gestão de Projetos | 8 | ⭐⭐⭐ |
| 2️⃣ | DbExer1SQLV4 | Varejo (Cupons) | 6 | ⭐⭐ |
| 3️⃣ | Hospital-SHU | Saúde | 12 | ⭐⭐⭐⭐ |
| 4️⃣ | Distribuidora | Logística | 10 | ⭐⭐⭐⭐ |
| 5️⃣ | Clínica Veterinária | Saúde Animal | 9 | ⭐⭐⭐ |

---

## 1️⃣ DbProjetos_Aram - Organização de Projetos

### 📋 Descrição
Sistema de gestão de projetos corporativos com controle de colaboradores, departamentos e alocação de recursos.

### 🎯 Funcionalidades Modeladas
- Gestão de colaboradores e departamentos
- Controle de projetos com múltiplos responsáveis
- Alocação de recursos por projeto
- Relacionamentos de dependência entre colaboradores
- Histórico de participação em projetos

### 🔍 Entidades Principais
- **Colaborador** (PK: id_colaborador)
- **Projeto** (PK: id_projeto)
- **Departamento** (PK: id_departamento)
- **Alocacao** (Associativa N:M)

### 📊 Diagrama

<img width="650" alt="DbProjetos_Aram" src="https://github.com/user-attachments/assets/e9ac35dd-7fb1-4849-9171-5e3b8667ee72" />

### 💡 Destaques Técnicos
- ✅ Relacionamento recursivo (Colaborador supervisiona Colaborador)
- ✅ Tabela associativa com atributos próprios (Alocacao)
- ✅ Integridade referencial completa
- ✅ Normalização até 3FN

---

## 2️⃣ DbExer1SQLV4 - Sistema de Cupons de Supermercado

### 📋 Descrição
Sistema de gestão de cupons fiscais e produtos de supermercado com controle de vendas e estoque.

### 🎯 Funcionalidades Modeladas
- Emissão de cupons fiscais
- Registro de produtos vendidos
- Controle de estoque por produto
- Categorização de produtos
- Relacionamento produto-cupom (itens vendidos)

### 🔍 Entidades Principais
- **Cupom** (PK: id_cupom)
- **Produto** (PK: id_produto)
- **Categoria** (PK: id_categoria)
- **Item_Cupom** (Associativa N:M)

### 📊 Diagrama

<img width="957" alt="DbExer1SQLV4" src="https://github.com/user-attachments/assets/b4c634e1-7f35-428f-8e73-1cc5fab56f52" />

### 💡 Destaques Técnicos
- ✅ Tabela associativa com quantidade e preço unitário
- ✅ Relacionamento 1:N entre Categoria e Produto
- ✅ Atributos calculáveis (valor total do cupom)
- ✅ Design otimizado para consultas de vendas

---

## 3️⃣ Hospital-SHU - Sistema Hospitalar

### 📋 Descrição
Sistema complexo de gestão hospitalar completo, incluindo pacientes, médicos, consultas, internações e prescrições.

### 🎯 Funcionalidades Modeladas
- Cadastro de pacientes e médicos
- Agendamento e registro de consultas
- Controle de internações e leitos
- Sistema de prescrições médicas
- Gestão de convênios médicos
- Especialidades médicas
- Histórico médico completo

### 🔍 Entidades Principais
- **Paciente** (PK: id_paciente)
- **Medico** (PK: id_medico)
- **Consulta** (PK: id_consulta)
- **Internacao** (PK: id_internacao)
- **Prescricao** (PK: id_prescricao)
- **Convenio** (PK: id_convenio)
- **Especialidade** (PK: id_especialidade)
- **Leito** (PK: id_leito)

### 📊 Diagrama

![modelagem-logica_hospital-shu](https://github.com/user-attachments/assets/49053919-f545-4d67-bc30-ae5b1ac83a6e)

### 💡 Destaques Técnicos
- ✅ **Alta complexidade** - 12 entidades inter-relacionadas
- ✅ Relacionamento N:M entre Médico e Especialidade
- ✅ Múltiplos níveis de relacionamento (Paciente → Consulta → Prescrição)
- ✅ Controle de status (consulta agendada/realizada, leito ocupado/livre)
- ✅ Integridade temporal (datas de consulta, período de internação)

---

## 4️⃣ Distribuidora - Sistema de Logística e Distribuição

### 📋 Descrição
Sistema robusto de gestão de distribuidora com controle de pedidos, estoque, fornecedores e entregas.

### 🎯 Funcionalidades Modeladas
- Gestão de fornecedores e produtos
- Controle de pedidos de compra
- Gerenciamento de estoque por armazém
- Sistema de entregas e rastreamento
- Relacionamento com transportadoras
- Controle de categorias de produtos

### 🔍 Entidades Principais
- **Fornecedor** (PK: id_fornecedor)
- **Produto** (PK: id_produto)
- **Pedido** (PK: id_pedido)
- **Estoque** (PK: id_estoque)
- **Entrega** (PK: id_entrega)
- **Transportadora** (PK: id_transportadora)
- **Armazem** (PK: id_armazem)

### 📊 Diagrama

<img width="1278" alt="Distribuidora" src="https://github.com/user-attachments/assets/2d471199-278e-42ed-911a-fedfb565b536" />

### 💡 Destaques Técnicos
- ✅ **Sistema complexo de logística** - Rastreamento completo
- ✅ Relacionamento ternário (Produto-Armazem-Estoque)
- ✅ Controle de status de pedidos e entregas
- ✅ Múltiplos níveis de agregação (Pedido → Item → Produto)
- ✅ Integridade referencial em cascata

---

## 5️⃣ Clínica Veterinária - Sistema de Atendimento Animal

### 📋 Descrição
Sistema completo de gestão de clínica veterinária com controle de pets, tutores, consultas e tratamentos.

### 🎯 Funcionalidades Modeladas
- Cadastro de tutores e animais de estimação
- Registro de consultas veterinárias
- Controle de vacinações e histórico médico
- Prescrições de medicamentos
- Agendamento de retornos
- Especialidades veterinárias
- Raças e espécies catalogadas

### 🔍 Entidades Principais
- **Tutor** (PK: id_tutor)
- **Pet** (PK: id_pet)
- **Veterinario** (PK: id_veterinario)
- **Consulta** (PK: id_consulta)
- **Vacina** (PK: id_vacina)
- **Raca** (PK: id_raca)
- **Especie** (PK: id_especie)
- **Medicamento** (PK: id_medicamento)

### 📊 Diagrama

<img width="1129" alt="Clínica Veterinária" src="https://github.com/user-attachments/assets/34028386-2a88-403c-b1ed-a33af6de6b90" />

### 💡 Destaques Técnicos
- ✅ Relacionamento 1:N (Tutor possui múltiplos Pets)
- ✅ Histórico médico completo por animal
- ✅ Controle de vacinações com datas
- ✅ Relacionamento N:M (Pet-Vacina através de Vacinacao)
- ✅ Taxonomia animal (Espécie → Raça → Pet)

---

## 🎓 Conceitos Aplicados

### 📚 Fundamentos de Modelagem

#### Entidades
- Representação de objetos do mundo real
- Atributos descritivos
- Chaves primárias únicas

#### Relacionamentos
- **1:1** - Um para um (raro, mas aplicado)
- **1:N** - Um para muitos (mais comum)
- **N:M** - Muitos para muitos (requer tabela associativa)

#### Cardinalidade
- **Mínima** - Obrigatoriedade (0 ou 1)
- **Máxima** - Quantidade permitida (1 ou N)

#### Normalização
- **1FN** - Atomicidade de atributos
- **2FN** - Dependência funcional total
- **3FN** - Ausência de dependências transitivas

### 🔧 Boas Práticas Aplicadas

✅ **Nomenclatura padronizada** - snake_case para tabelas e colunas  
✅ **Prefixos** - id_ para chaves primárias, fk_ para estrangeiras  
✅ **Integridade referencial** - Todas as FKs com constraints  
✅ **Normalização** - Até 3FN em todos os diagramas  
✅ **Tipos de dados apropriados** - VARCHAR, INT, DATE, DECIMAL  
✅ **Constraints** - NOT NULL, UNIQUE, CHECK quando aplicável  

---

## 🛠️ Stack Tecnológica

### Ferramentas de Modelagem
![MySQL](https://img.shields.io/badge/MySQL_Workbench-4479A1?style=flat-square&logo=mysql&logoColor=white)
![Oracle](https://img.shields.io/badge/Oracle_Data_Modeler-F80000?style=flat-square&logo=oracle&logoColor=white)

### SGBDs Compatíveis
![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=flat-square&logo=mysql&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-316192?style=flat-square&logo=postgresql&logoColor=white)
![SQL Server](https://img.shields.io/badge/SQL_Server-CC2927?style=flat-square&logo=microsoft-sql-server&logoColor=white)
![Oracle DB](https://img.shields.io/badge/Oracle_DB-F80000?style=flat-square&logo=oracle&logoColor=white)
  
---

## 📊 Comparativo de Complexidade

### Matriz de Características

| Diagrama | Entidades | Relacionamentos | Tabelas Associativas | Níveis de Profundidade |
|----------|-----------|-----------------|---------------------|------------------------|
| **DbProjetos** | 8 | 10 | 1 | 3 |
| **Cupons** | 6 | 5 | 1 | 2 |
| **Hospital** | 12 | 15 | 2 | 4 |
| **Distribuidora** | 10 | 13 | 2 | 4 |
| **Veterinária** | 9 | 11 | 2 | 3 |

### Nível de Dificuldade

🟢 **Básico:** DbExer1SQLV4 (Cupons)  
🟡 **Intermediário:** DbProjetos, Clínica Veterinária  
🔴 **Avançado:** Hospital, Distribuidora  

---

## 🎯 Casos de Uso

### Para Estudantes
- 📚 **Aprender modelagem** - Exemplos práticos
- 🎓 **Referência para trabalhos** - Templates de qualidade
- 💡 **Inspiração** - Diferentes domínios de negócio

### Para Desenvolvedores
- 🔧 **Base para projetos** - Arquitetura inicial
- 📝 **Documentação** - Estrutura de dados clara
- 🚀 **Prototipagem rápida** - Scripts DDL prontos

### Para Recrutadores
- ✅ **Avaliação de competências** - Portfólio técnico
- 💼 **Prova de experiência** - Projetos reais
- 📊 **Nível de conhecimento** - Complexidade demonstrada

---

## 🎓 Contexto Acadêmico

### Formação
**Curso:** Técnico em Ciência de Dados  
**Instituição:** CEDUP Timbó - SC  
**Ano:** 2023-2025  

### Disciplinas Relacionadas
- Banco de Dados Relacional
- Modelagem de Dados
- SQL Avançado
- Arquitetura de Sistemas

### Competências Desenvolvidas

1. **🗄️ Modelagem de Dados** - Conceitual, lógica e física
2. **🔗 Relacionamentos** - Todos os tipos de cardinalidade
3. **🧹 Normalização** - Até 3FN
4. **🔧 Ferramentas** - MySQL Workbench e Oracle Data Modeler
5. **📝 Documentação** - Diagramas claros e autoexplicativos
6. **💡 Análise de Requisitos** - Tradução de negócio em dados

---

## 🚀 Próximos Passos

### Melhorias Planejadas

- [ ] **Scripts de povoamento** - Dados de exemplo para cada diagrama
- [ ] **Stored procedures** - Lógica de negócio em SQL
- [ ] **Views** - Consultas complexas pré-definidas
- [ ] **Índices** - Otimização de performance
- [ ] **Triggers** - Automatização de regras de negócio
- [ ] **Documentação detalhada** - Descrição de cada tabela e coluna

### Novos Diagramas em Desenvolvimento

- [ ] Sistema de E-commerce
- [ ] Gestão de Biblioteca
- [ ] Controle de Estoque de Farmácia
- [ ] Sistema de Academia
- [ ] Plataforma de Cursos Online

---

## 🤝 Contribuindo

Sugestões e melhorias são bem-vindas!

### Como Contribuir

1. Fork o projeto
2. Crie uma branch (`git checkout -b melhoria/novo-diagrama`)
3. Commit suas mudanças (`git commit -m 'Adiciona diagrama X'`)
4. Push para a branch (`git push origin melhoria/novo-diagrama`)
5. Abra um Pull Request

### Áreas de Contribuição

- 🗄️ **Novos diagramas** - Outros domínios de negócio
- 🔧 **Otimizações** - Melhorias em diagramas existentes
- 📝 **Documentação** - Descrições mais detalhadas
- 💾 **Scripts** - DDL, DML, Procedures
- 🐛 **Correções** - Erros de modelagem

---

## 📝 Licença

Este projeto foi desenvolvido para fins **educacionais** e está disponível para:

✅ Uso em estudos e aprendizado  
✅ Modificação e adaptação  
✅ Distribuição com créditos  
✅ Uso em projetos acadêmicos  

---

## 📞 Contato

**Desenvolvedor:** Aram Bohmann Leite da Luz

[![Email](https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:arambohmannleitedaluz@gmail.com)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/aram-luz-1b0ab1321)
[![GitHub](https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/Aram-Bohmann)
[![Portfolio](https://img.shields.io/badge/Portfolio-FF5722?style=for-the-badge&logo=google-chrome&logoColor=white)](https://aram-bohmann.github.io/Site-Portfolio/)

---

## 🙏 Agradecimentos

- **CEDUP Timbó** - Formação técnica de excelência
- **MySQL** - Ferramenta robusta de modelagem
- **Oracle** - Data Modeler profissional
- **Comunidade de Dados** - Compartilhamento de conhecimento

---

<div align="center">

### ⭐ Se este projeto foi útil para você, considere dar uma estrela!

**Desenvolvido com 💙 e 🗄️ como parte da formação em Ciência de Dados**

*"Dados bem modelados são a base de sistemas robustos"*

</div>
