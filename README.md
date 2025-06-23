# 📰 Toughts - NODE

O ***Toughts*** é um projeto desenvolvido sobre orientação de Node.js e organização estrutual MVC em JavaScript durante o curso oferecido pela Hora de Codar. Ele permite que os usuários criem contas, gerencie suas contas e adicionem e removam pensamentos proporcionando uma interface interativa e dinâmica. O código implementa uma lógica para gerenciar as pensamentos, garantindo que a interface seja atualizada automaticamente conforme o usuário interage com a aplicação.

----------------------------

## 🌐 Interface Web

A página inicial apresenta uma interface escura e moderna, focada na exibição de pensamentos públicos criados por usuários da plataforma. A navegação é limpa, com elementos bem espaçados e destaque para o conteúdo textual.

![Página Principal](/public/img/print1.png)

----------------------------

### 🔍 Testando Localmente

Para testar o projeto localmente, siga estas etapas:

1. Abra o terminal (ou prompt de comando) e execute o seguinte comando para clonar o repositório:

   `git clone https://github.com/joaocastro95/toughts.git`

2. Após clonar o repositório, abra o terminal e vá até a pasta clonada.
   
   `cd caminho/para/a/pasta/do/projeto`

3. Instale as dependências.

  `npm install`
   
4. Inicialize o projeto.

   `npm start`

5. Abra a porta no navegador.

   `http://localhost:3000/`

Isso abrirá a interface web do projeto. Se o servidor estiver funcionando corretamente, você verá a página principal onde poderá utilizar o "Toughts".


#### 📝 Observação
Se você encontrar algum problema ou a página não carregar, consulte a seção de [Autores](#-autores) e entre em contato conosco.

----------------------------

## 🚀 Estrutura do Projeto
Mantivemos uma estrutura organizada para facilitar a manutenção e a compreensão do código:

### ⚙️**Backend**

- **`controllers/`**  
  - `AuthController.js`: Controlador responsável pelas ações de login, logout e registro de usuários.  
  - `ToughtController.js`: Lógica de CRUD dos pensamentos (criar, listar, editar, deletar, dashboard, busca).  

- **`db/`**  
  - `conn.js`: Configuração da conexão com o banco de dados utilizando Sequelize.  

- **`helpers/`**  
  - `auth.js`: Middleware auxiliar para proteger rotas e verificar autenticação de usuários.  

- **`models/`**  
  - `Tought.js`: Modelo Sequelize que representa os pensamentos.  
  - `User.js`: Modelo Sequelize que representa os usuários.  

- **`routes/`**  
  - `authRoutes.js`: Define as rotas para login e registro de usuários.  
  - `toughtsRoutes.js`: Define as rotas para criação, edição, exclusão e exibição de pensamentos.  

- **`index.js`**  
  Arquivo principal da aplicação. Inicializa o servidor Express, configura Handlebars, sessões, middlewares e sincroniza os modelos com o banco de dados.


### 🎨**Frontend**

- **`views/`**  
  - **`auth/`**  
    - `login.handlebars`: Página de login.  
    - `register.handlebars`: Página de registro.  

  - **`layouts/`**  
    - `main.handlebars`: Template base utilizado pelas demais views com cabeçalho, rodapé e estrutura HTML principal.  

  - **`toughts/`**  
    - `home.handlebars`: Página inicial com listagem de pensamentos públicos, busca e ordenação.  
    - `dashboard.handlebars`: Painel do usuário logado com seus próprios pensamentos.  
    - `create.handlebars`: Formulário para criar novos pensamentos.  
    - `edit.handlebars`: Formulário para editar pensamentos existentes.  

- **`public/css/`**  
  - `styles.css`: Arquivo principal de estilos da aplicação.  

- **`public/img/`**  
  - Pasta reservada para imagens usadas na interface (ícones, logos, etc).  


### **Sessões**

- **`sessions/`**  
  - Diretório utilizado para armazenar sessões da aplicação (dependente da configuração de sessão).


### **Configurações**

- **`.gitignore`**: Arquivo que define o que deve ser ignorado pelo Git (ex: `node_modules`, arquivos sensíveis, etc).  
- **`package.json`**: Arquivo de configuração do projeto Node.js com lista de dependências e scripts.  
- **`package-lock.json`**: Arquivo que registra as versões exatas das dependências instaladas.  
- **`README.md`**: Arquivo de documentação do projeto.  
- **`instalacoes.txt`**: Arquivo de anotações ou instruções internas relacionadas à instalação/configuração do projeto.

----------------------------

## 🚀 Tecnologias Utilizadas

| Ferramenta       | Descrição                                         |
| ---------------- | ------------------------------------------------- |
| ![Node.js](https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=nodedotjs&logoColor=white) | Ambiente de execução JavaScript backend |
| ![Express](https://img.shields.io/badge/Express-000000?style=for-the-badge&logo=express&logoColor=white) | Framework minimalista para construção do servidor web |
| ![Express-Handlebars](https://img.shields.io/badge/Handlebars.js-f0772b?style=for-the-badge&logo=handlebarsdotjs&logoColor=black) | Engine de templates utilizada para renderização HTML |
| ![Sequelize](https://img.shields.io/badge/Sequelize-52B0E7?style=for-the-badge&logo=sequelize&logoColor=white) | ORM para modelagem e comunicação com o MySQL |
| ![MySQL](https://img.shields.io/badge/MySQL-00758F?style=for-the-badge&logo=mysql&logoColor=white) | Banco de dados relacional utilizado |
| ![bcryptjs](https://img.shields.io/badge/bcryptjs-orange?style=for-the-badge) | Biblioteca para hash de senhas de forma segura |
| ![express-session](https://img.shields.io/badge/express--session-blue?style=for-the-badge) | Gerenciamento de sessões de usuários no servidor Express |
| ![connect-flash](https://img.shields.io/badge/connect--flash-lightgrey?style=for-the-badge) | Mensagens temporárias armazenadas na sessão (flash messages) |
| ![express-flash](https://img.shields.io/badge/express--flash-lightgrey?style=for-the-badge) | Flash messages integradas ao Express |
| ![cookie-parser](https://img.shields.io/badge/cookie--parser-yellowgreen?style=for-the-badge) | Middleware para manipulação de cookies HTTP |
| ![cookie-session](https://img.shields.io/badge/cookie--session-blueviolet?style=for-the-badge) | Sessão baseada em cookies como alternativa leve ao `express-session` |
| ![session-file-store](https://img.shields.io/badge/session--file--store-forestgreen?style=for-the-badge) | Armazenamento de sessões em arquivos locais |
| ![Nodemon](https://img.shields.io/badge/Nodemon-76D04B?style=for-the-badge&logo=nodemon&logoColor=white) | Monitoramento automático e reinício do servidor durante o desenvolvimento |
| ![HTML5/CSS3](https://img.shields.io/badge/HTML5%20/%20CSS3-E34F26?style=for-the-badge&logo=html5&logoColor=white) | Estrutura e estilização das páginas |
| ![VS Code](https://img.shields.io/badge/VS%20Code-007ACC?style=for-the-badge&logo=visual-studio-code&logoColor=white) | Editor de código utilizado |
| ![Windows](https://img.shields.io/badge/Windows-0078D6?style=for-the-badge&logo=windows&logoColor=white) | Sistema operacional de desenvolvimento |


## 📝 Autores

| [<img loading="lazy" src="https://avatars.githubusercontent.com/u/132524175?v=4" width=115><br><sub>João Castro</sub>](https://github.com/joaocastro95) |
| --- |