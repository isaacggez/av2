# 🔑 Tela de Login e Cadastro 

Este projeto consiste em uma tela de **Login** e **Cadastro** totalmente responsiva, desenvolvida em um único arquivo **HTML**, utilizando **Tailwind CSS** para estilização moderna e **JavaScript puro** para implementar a lógica de autenticação.  

O sistema utiliza o **localStorage** do navegador para persistir os dados dos usuários cadastrados e gerenciar o estado da sessão (usuário logado/deslogado), oferecendo uma experiência de usuário funcional e imediata. 🚀  

---

## 🚀 Funcionalidades Principais

| Funcionalidade           | Descrição                                                                                                                                   |
|--------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| **Cadastro de Usuário**  | Permite registrar um novo usuário com e-mail (único) e senha (mínimo de 6 caracteres). Não faz login automático, exigindo login posterior.  |
| **Login de Usuário**     | Autentica o usuário verificando as credenciais salvas no `localStorage`.                                                                    |
| **Alternância de Formulário** | Alterna de forma fluida entre as telas de "Acesso" (Login) e "Criar Conta" (Registro).                                                  |
| **Toggle de Senha (👁️ / ❌)** | Permite mostrar (👁️) ou esconder (❌) a senha digitada em ambos os formulários, oferecendo melhor usabilidade e segurança.             |
| **Persistência de Sessão**   | Mantém o usuário logado mesmo após o fechamento e reabertura do navegador, utilizando `localStorage`.                                   |
| **Sair da Conta**        | Botão funcional na tela pós-login que encerra a sessão, limpando o registro do usuário no `localStorage`.                                   |

---

## 🛠️ Tecnologias Utilizadas

- **HTML5**: Estrutura base do projeto.  
- **Tailwind CSS (via CDN)**: Framework CSS utilizado para toda a estilização e garantir um design totalmente responsivo e moderno.  
- **JavaScript Puro**: Responsável pela lógica de formulários, validações, alternância de tela e manipulação do `localStorage`.  

---

## 🔒 Persistência de Dados (localStorage)

Em um ambiente de produção, a autenticação seria feita por um backend (como Firebase ou servidor próprio), mas para simular o funcionamento real de forma simples, usamos o **localStorage**:

- **Chave de Usuários (`auth_users`)**: Armazena um objeto JSON onde as chaves são os e-mails dos usuários e os valores são as suas senhas.  
  ⚠️ Importante: Este método é apenas para fins de **demonstração local**. Senhas nunca devem ser salvas em texto puro no `localStorage` em aplicações reais, devido a riscos de segurança.  

- **Chave de Sessão (`current_user`)**: Armazena o e-mail do usuário atualmente logado. Se esta chave estiver preenchida, o sistema considera o usuário como autenticado.  

---

## ⚙️ Como Usar (Fluxo de Autenticação)

### 🔹 Criar Conta
1. Clique em **"Crie sua Conta"**.  
2. Preencha um e-mail válido e uma senha (mínimo 6 caracteres).  
3. Ao clicar em **Registrar**, o usuário é salvo no `localStorage` e você volta para a tela de Acesso.  

### 🔹 Acesso
1. Use o e-mail e a senha que você acabou de cadastrar.  
2. Ao clicar em **Entrar**, se as credenciais estiverem corretas, a tela de Login é escondida e a **Tela Pós-Login** é exibida.  

### 🔹 Sair da Conta
- Na Tela Pós-Login, clique em **Sair da Conta**. Isso remove o `current_user` do `localStorage` e retorna para o formulário de Login.  

### 🔹 Recuperação de Sessão
- Se você fizer login e **recarregar a página**, o JavaScript verifica o `localStorage` e o mantém na Tela Pós-Login.  

---

## 📸 Preview do Projeto

Tela de **Login e Cadastro**:  
![Login e Cadastro](https://i.imgur.com/AqKInZR.png)  

Tela de **Cadastro (Criar Conta)**:  
![Criar Conta](https://i.imgur.com/Mb8YfGq.png)  

Tela **Pós-Login**:  
![Tela Pós-Login](https://i.imgur.com/SoHnvBT.png)  

---
