# PortEdu App

## 📚 Sobre o Projeto

O PortEdu App é uma aplicação web front-end desenvolvida para a plataforma educacional PortEdu. Este sistema tem como objetivo facilitar a criação, gestão e compartilhamento de portfólios docentes, permitindo que educadores documentem suas práticas pedagógicas, conquistas profissionais e desenvolvimento contínuo.

## 🎯 Propósito

A plataforma PortEdu foi criada para:

- Centralizar informações sobre a trajetória profissional de educadores
- Promover a reflexão sobre práticas pedagógicas
- Facilitar o compartilhamento de experiências entre professores
- Documentar o desenvolvimento profissional contínuo
- Criar um espaço de valorização do trabalho docente

## ✨ Funcionalidades Principais

### 1. Gestão de Portfólio

- Criação e edição de portfólios personalizados
- Upload de documentos, imagens e vídeos
- Organização por categorias e tags
- Controle de visibilidade (público/privado)

### 2. Perfil Profissional

- Informações pessoais e acadêmicas
- Histórico de formação
- Experiências profissionais
- Certificações e cursos

### 3. Projetos e Atividades

- Documentação de projetos pedagógicos
- Registro de atividades desenvolvidas
- Evidências de aprendizagem dos alunos
- Reflexões sobre a prática docente

### 4. Compartilhamento e Colaboração

- Compartilhamento de portfólios com colegas
- Comentários e feedbacks
- Comunidade de educadores
- Inspiração e troca de experiências

## 🚀 Instruções Iniciais

### Pré-requisitos

Antes de começar, certifique-se de ter instalado:

```bash
Node.js >= 16.x
npm >= 8.x ou yarn >= 1.22
```

### Instalação

1. Clone o repositório:

```bash
git clone https://github.com/PortEdu/portedu-app.git
cd portedu-app
```

2. Instale as dependências:

```bash
npm install
# ou
yarn install
```

3. Configure as variáveis de ambiente:

```bash
cp .env.example .env
```

4. Execute o projeto em modo de desenvolvimento:

```bash
npm run dev
# ou
yarn dev
```

O aplicativo estará disponível em `http://localhost:3000`

## 📦 Modelos de Dados Educacionais

O PortEdu App trabalha com os seguintes modelos de dados principais:

### Artefato

Representa qualquer material ou evidência produzida pelo educador.

```json
{
  "id": "artefato1",
  "titulo": "Plano de Aula de Ciências",
  "descricao": "Plano de aula focado em experimentos químicos para alunos do ensino fundamental.",
  "tipo": "Documento",
  "data_criacao": "2025-03-10",
  "autor": "Prof. João Silva",
  "competencias_relacionadas": ["competencia1"],
  "url": "https://drive.google.com/arquivo123"
}
```

### Competência

Define uma habilidade, conhecimento ou atitude do educador conforme a BNCC.

```json
{
  "id": "competencia1",
  "nome": "Pensamento Científico",
  "descricao": "Promover o desenvolvimento do pensamento crítico e científico em sala de aula.",
  "referencia_bncc": "CI 05EF12",
  "artefatos": ["artefato1"]
}
```

### Rubrica

Critérios e níveis de avaliação para um determinado objetivo de aprendizagem.

```json
{
  "id": "rubrica1",
  "nome": "Avaliação de Experimento de Química",
  "criterios": [
    "Preparação dos materiais",
    "Execução do experimento",
    "Interpretação dos resultados"
  ],
  "niveis": [
    "Inicial",
    "Intermediário",
    "Avançado"
  ],
  "artefatos_atingidos": ["artefato1"]
}
```

### MetaCPD

Meta de desenvolvimento profissional contínuo do docente.

```json
{
  "id": "metacpd1",
  "descricao": "Participar de curso sobre metodologias ativas",
  "data_inicio": "2025-04-01",
  "data_fim": "2025-05-10",
  "status": "Em andamento",
  "artefatos_produzidos": ["artefato1"]
}
```

## 🤝 Instruções para Codificação Colaborativa

### Como Contribuir

Agradecemos seu interesse em contribuir com o PortEdu App! Para garantir uma colaboração eficiente e organizada, siga as diretrizes abaixo:

#### 1. Configuração do Ambiente

Antes de começar a desenvolver, certifique-se de:

- Fazer um fork do repositório para sua conta do GitHub
- Clonar o fork para sua máquina local
- Adicionar o repositório original como remote upstream:

```bash
git remote add upstream https://github.com/PortEdu/portedu-app.git
```

#### 2. Organização dos Diretórios

O projeto segue a seguinte estrutura de diretórios:

```
portedu-app/
├── src/
│   ├── components/     # Componentes React reutilizáveis
│   ├── pages/          # Páginas e rotas da aplicação
│   ├── services/       # Serviços de API e integrações
│   ├── hooks/          # Custom hooks do React
│   ├── utils/          # Funções utilitárias e helpers
│   ├── styles/         # Arquivos de estilo global
│   ├── assets/         # Imagens, ícones e outros recursos
│   ├── contexts/       # Contextos do React para estado global
│   └── types/          # Definições de tipos TypeScript
├── public/             # Arquivos públicos estáticos
├── tests/              # Testes automatizados
└── docs/               # Documentação adicional
```

**Convenções importantes:**

- Componentes devem ser criados em pastas individuais dentro de `src/components/`
- Cada componente deve incluir seus próprios estilos e testes
- Use PascalCase para nomes de componentes (ex: `ProfileCard.tsx`)
- Use camelCase para funções e variáveis utilitárias
- Mantenha os arquivos organizados por funcionalidade, não por tipo

#### 3. Padrões de Código

- **Idioma:** Todo o código, comentários e documentação devem estar em **português**
- **Estilo:** Seguimos as convenções do ESLint configuradas no projeto
- **Commits:** Use mensagens de commit claras e descritivas em português:
  - `feat: adiciona componente de upload de arquivos`
  - `fix: corrige bug no formulário de edição de perfil`
  - `docs: atualiza documentação do README`
  - `style: ajusta espaçamento nos componentes`
  - `refactor: reorganiza estrutura de pastas`
  - `test: adiciona testes para o módulo de autenticação`

#### 4. Fluxo de Trabalho para Contribuições

**Passo 1:** Crie uma branch para sua funcionalidade ou correção

```bash
git checkout -b feature/nome-da-funcionalidade
# ou
git checkout -b fix/nome-do-bug
```

**Passo 2:** Desenvolva sua contribuição

- Escreva código limpo e bem documentado
- Adicione testes para novas funcionalidades
- Certifique-se de que todos os testes existentes continuam passando
- Mantenha os commits pequenos e focados

**Passo 3:** Mantenha sua branch atualizada

```bash
git fetch upstream
git rebase upstream/main
```

**Passo 4:** Execute os testes e validações

```bash
npm run test
npm run lint
npm run build
```

**Passo 5:** Envie suas alterações para seu fork

```bash
git push origin feature/nome-da-funcionalidade
```

#### 5. Como Enviar Pull Requests

1. **Acesse o GitHub** e vá para o repositório original do PortEdu App
2. **Clique em "New Pull Request"**
3. **Selecione sua branch** do fork como origem
4. **Preencha o template do PR** com as seguintes informações:
   - **Título:** Descrição clara e concisa da mudança
   - **Descrição:** Explique o que foi alterado e por quê
   - **Issue relacionada:** Referencie issues relacionadas (ex: `Closes #123`)
   - **Testes realizados:** Descreva como testou as mudanças
   - **Capturas de tela:** Adicione prints se houver mudanças visuais

5. **Aguarde a revisão:** Os mantenedores do projeto revisarão seu PR e poderão solicitar alterações
6. **Responda aos comentários:** Faça as alterações solicitadas e atualize o PR

#### 6. Boas Práticas

- ✅ Leia toda a documentação antes de começar
- ✅ Comunique-se através das issues antes de iniciar grandes mudanças
- ✅ Mantenha o código simples e legível
- ✅ Documente funções e componentes complexos
- ✅ Escreva testes para novas funcionalidades
- ✅ Respeite o código de conduta do projeto
- ✅ Seja receptivo ao feedback da equipe
- ❌ Não misture múltiplas funcionalidades em um único PR
- ❌ Não faça commits direto na branch main
- ❌ Não ignore os padrões de código estabelecidos

#### 7. Precisa de Ajuda?

Se tiver dúvidas ou precisar de orientação:

- Abra uma issue com a tag `question`
- Consulte a documentação no diretório `docs/`
- Entre em contato com os mantenedores do projeto

**Obrigado por contribuir com o PortEdu App! Juntos, estamos construindo uma ferramenta valiosa para educadores. 🎓✨**
