# 🏥 Clínica VidaPlena — Sistema de Gestão

![Java](https://img.shields.io/badge/Java-JDK_11+-ED8B00?style=flat-square&logo=openjdk&logoColor=white)
![POO](https://img.shields.io/badge/Paradigma-Orientação_a_Objetos-2b6cb0?style=flat-square)
![Status](https://img.shields.io/badge/Status-Concluído_(AV2)-success?style=flat-square)

Sistema de gestão para clínica multidisciplinar desenvolvido como projeto avaliativo da disciplina de **Programação Orientada a Objetos** — UNIPÊ. A AV2 representa a evolução do sistema da AV1, incorporando os conceitos avançados de POO estudados ao longo da disciplina.

---

## 📋 Funcionalidades

- **Pacientes e Convênios** — Cadastro com validação de dados, vínculos com planos de saúde e controle de status ativo/inativo
- **Profissionais** — Cadastro por especialidade (Clínico Geral, Fisioterapeuta, Psicólogo, Nutricionista) com gestão de horários
- **Consultas** — Agendamento com controle de conflitos, cancelamento com regras de multa e remarcação
- **Prontuários** — Registro clínico de atendimentos com composição estrita
- **Pagamentos** — Processamento polimórfico para Dinheiro/Pix, Cartão e Convênio com cálculo automático de descontos
- **Relatórios** — Visualização de dados por profissional, período e resumo financeiro

---

## 🧠 Conceitos de POO Aplicados

| Requisito | Conceito | Onde foi aplicado |
|-----------|----------|-------------------|
| R1/R2 | Encapsulamento e modificadores | Atributos `private`/`protected`, validações em setters (CPF, idade) |
| R3 | Herança profunda (3+ níveis) | `Pessoa` → `Profissional` → `Fisioterapeuta` |
| R4 | Sobrecarga e Sobrescrita | Construtores múltiplos, `@Override` com `exibirResumo()` |
| R5 | Ligação dinâmica | `List<Pessoa>` percorrida com comportamento polimórfico |
| R6 | Classes abstratas | `Pessoa` e `Pagamento` abstratas |
| R7 | Interfaces | `Agendavel` e `Exportavel` implementadas por múltiplas classes |
| R8 | Associação, Agregação e Composição | Paciente→Convênio, Profissional→Horários, Atendimento→Prontuário |
| R9 | Exceções personalizadas | `PacienteInativoException`, `ConvenioNaoCobreException`, etc. |
| R10 | Coleções | `ArrayList`, `HashSet` e `HashMap` substituindo arrays fixos |

---

## ⚙️ Como Executar

**Pré-requisito:** JDK 11 ou superior instalado.

```bash
# 1. Clone o repositório
git clone https://github.com/SeuUsuario/VidaPlena.git

# 2. Entre na pasta do código-fonte
cd VidaPlena/src

# 3. Compile
javac br/com/vidaplena/Main.java

# 4. Execute
java br.com.vidaplena.Main
```

---

## 🗂️ Estrutura do Projeto
src/

└── br/com/vidaplena/

├── Main.java

├── exceptions/        # Exceções personalizadas

├── interfaces/        # Agendavel, Exportavel

├── service/           # ClinicaServico (regras de negócio)

└── model/

├── pessoas/       # Pessoa, Paciente, Convenio

├── profissionais/ # Profissional e especializações

├── atendimentos/  # Consulta, Atendimento, Prontuario

└── pagamentos/    # Pagamento e formas de pagamento

---

## 👥 Equipe

| Integrante | Responsabilidade |
|------------|-----------------|
| Eduardo Ramalho Teixeira | Pessoas e Convênios |
| Renan de Araújo Venturini Silva | Agendamentos e Prontuários |
| Robson Windson Dantas de Almeida | Faturamento e Finanças |
| João Victor Ferreira da Costa | (especialidade) |
| Integrante 5 | Interfaces e Relatórios |
| Integrante 6 | Exceções Personalizadas |
| Integrante 7 | Serviço e Interface (Main) |

---

> Disciplina de Programação Orientada a Objetos — UNIPÊ  
> Professor: Jonatas Pereira Cabral de Araujo
