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
```
bash
Node.js >= 16.x
npm >= 8.x ou yarn >= 1.22
```
### Instalação
1. Clone o repositório:
```
bash
git clone https://github.com/PortEdu/portedu-app.git
cd portedu-app
```
2. Instale as dependências:
```
bash
npm install
# ou
yarn install
```
3. Configure as variáveis de ambiente:
```
bash
cp .env.example .env
```
**Desenvolvido com ❤️ para educadores**

## 📦 Modelos de Dados Educacionais

### Artefato
Representa qualquer evidência ou objeto digital relacionado à prática pedagógica.
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
