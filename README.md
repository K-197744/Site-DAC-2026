## Sobre o Projeto

O **EquipFlow** é um protótipo web full stack desenvolvido para controlar o fluxo de empréstimo e devolução de equipamentos didáticos do cenário fictício **NRDT (Núcleo de Recursos Didáticos em Tecnologia)**. O projeto foi criado no contexto do DAC 2026 do curso de TADS da UCDB, com foco em organização, rastreabilidade, acessibilidade e eficiência operacional.

A proposta surgiu para solucionar problemas comuns em laboratórios e núcleos de recursos compartilhados, onde o controle normalmente depende de planilhas, formulários em papel ou mensagens informais. Esse modelo dificulta a rastreabilidade dos equipamentos, gera conflitos de uso, aumenta o retrabalho administrativo e reduz a visibilidade do acervo disponível.

O EquipFlow centraliza todas essas informações em uma única plataforma acessível pelo navegador, permitindo acompanhar o ciclo completo de solicitação, aprovação, empréstimo e devolução dos equipamentos.

---

## Problema Identificado

No cenário do NRDT, equipamentos como notebooks, projetores, kits de prototipagem e instrumentos eletrônicos são compartilhados entre docentes e estudantes para aulas, eventos e projetos acadêmicos.

Sem um sistema integrado, diversos problemas operacionais podem ocorrer:

* Falta de controle sobre quem retirou determinado equipamento
* Dificuldade para acompanhar prazos de devolução
* Conflitos de reserva e disponibilidade
* Perda de histórico de empréstimos
* Retrabalho administrativo em conferências manuais
* Dependência de planilhas descentralizadas
* Falta de transparência sobre o acervo disponível

O EquipFlow foi pensado justamente para reduzir esses problemas através de uma solução digital centralizada e organizada.

---

## Objetivo do Sistema

O principal objetivo do projeto é oferecer uma plataforma web funcional para gerenciamento de patrimônio didático, permitindo:

* Cadastro e gerenciamento de equipamentos
* Controle de disponibilidade do acervo
* Solicitação formal de empréstimos
* Aprovação ou recusa de pedidos
* Registro de devoluções
* Histórico completo de utilização
* Rastreabilidade das operações
* Maior organização administrativa

Além disso, o projeto busca aplicar na prática conceitos estudados durante o curso, integrando front-end, back-end, banco de dados, autenticação e APIs REST.

---

## Perfis de Usuário

### Administrador

Responsável pelo gerenciamento do patrimônio do NRDT.

Funcionalidades:

* Cadastrar equipamentos
* Editar informações do patrimônio
* Alterar status dos itens
* Aprovar ou recusar solicitações
* Acompanhar empréstimos ativos
* Visualizar histórico completo
* Monitorar indicadores do sistema

### Solicitante

Representa docentes ou estudantes autorizados a utilizar os equipamentos.

Funcionalidades:

* Consultar catálogo disponível
* Visualizar ficha do equipamento
* Solicitar empréstimos
* Aceitar termo de responsabilidade
* Acompanhar status dos pedidos
* Registrar devolução dos itens

---

## Fluxo de Funcionamento

O sistema segue um fluxo simples e organizado:

**Solicitação → Aprovação → Empréstimo ativo → Devolução**

1. O solicitante escolhe um equipamento disponível
2. Define as datas de retirada e devolução
3. Aceita o termo de responsabilidade
4. O pedido fica pendente até análise do administrador
5. O administrador aprova ou recusa a solicitação
6. Após aprovação, o empréstimo se torna ativo
7. O usuário registra a devolução ao final do uso
8. O equipamento volta ao status disponível

O sistema também aplica validações importantes:

* Prazo mínimo de empréstimo
* Bloqueio de itens em manutenção
* Controle de disponibilidade
* Registro do aceite do termo
* Histórico completo das operações

---

## Tecnologias Utilizadas

| Camada         | Tecnologias                  |
| -------------- | ---------------------------- |
| Front-end      | React 19 · TypeScript · Vite |
| Back-end       | Python · FastAPI             |
| Banco de Dados | SQLite                       |
| ORM            | SQLAlchemy                   |
| Autenticação   | JWT · bcrypt                 |

---

## Arquitetura da Aplicação

O EquipFlow utiliza arquitetura web full stack baseada em API REST.

O front-end foi desenvolvido em React com TypeScript, proporcionando uma interface moderna, responsiva e componentizada. Já o back-end utiliza FastAPI, responsável pelas regras de negócio, autenticação e gerenciamento dos dados.

A comunicação entre cliente e servidor ocorre via JSON utilizando endpoints REST protegidos por autenticação JWT.

Essa estrutura permite:

* Separação entre interface e lógica de negócio
* Melhor organização do código
* Facilidade de manutenção
* Possibilidade de expansão futura
* Integração com outros sistemas

---

## Interface e Experiência do Usuário

A interface foi projetada para oferecer clareza visual e facilidade de navegação.

Entre os recursos implementados estão:

* Tema claro e escuro
* Layout responsivo
* Feedback visual de ações
* Modais interativos
* Painéis organizados por perfil
* Indicadores visuais de status
* Tabelas e gráficos administrativos

O sistema também considera práticas de acessibilidade digital:

* Contraste adequado
* Navegação simplificada
* Compatibilidade com leitores de tela
* Labels descritivos
* Suporte a redução de animações

---

## API REST e Documentação

A API possui documentação automática gerada pelo Swagger através do FastAPI.

Principais grupos de rotas:

* Autenticação
* Equipamentos
* Empréstimos
* Health Check

A documentação permite visualizar:

* Endpoints disponíveis
* Estrutura dos dados
* Métodos HTTP
* Testes das rotas diretamente pelo navegador

---

## Estrutura de Dados

### Usuário

Armazena informações de login, nome, senha criptografada e perfil de acesso.

### Equipamento

Contém os dados patrimoniais dos itens, incluindo nome, descrição, código e situação atual.

### Empréstimo

Registra todo o fluxo da solicitação:

* datas
* usuário responsável
* equipamento
* status
* aprovação
* devolução
* aceite do termo

---

## Considerações Finais

O EquipFlow demonstra como tecnologias web modernas podem ser utilizadas para resolver problemas reais de organização e controle de patrimônio em ambientes acadêmicos.

Além de servir como projeto prático para aplicação dos conteúdos estudados em TADS, o sistema também evidencia conceitos importantes de:

* desenvolvimento full stack
* APIs REST
* autenticação segura
* modelagem de banco de dados
* experiência do usuário
* acessibilidade
* integração entre sistemas

O projeto possui caráter exclusivamente acadêmico e utiliza dados fictícios para fins educacionais e de apresentação.
