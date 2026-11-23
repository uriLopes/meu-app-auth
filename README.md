# Meu App Auth (Expo + Neon Auth)

Aplicativo React Native com Expo e **Neon Auth (Managed Better Auth)** construído em JavaScript puro, sem bibliotecas externas de navegação e sem SDKs pesados de autenticação.

## Funcionalidades

- **Cadastro:** Criação de usuário com nome, e-mail e senha diretamente no banco PostgreSQL gerenciado pelo Neon (`neon_auth.user`).
- **Login:** Autenticação via API REST (`/sign-in/email`) com gerenciamento de cookies de sessão nativo.
- **Área Logada:** Exibição do nome, e-mail e ID do usuário cadastrado, com opção de Logout.
- **Multiplataforma:** Compatível com Android, iOS (via Expo Go) e Navegador Web.

## Estrutura do Projeto

```
meu-app-auth/
├── assets/                  # Ícones e imagens do Expo
├── src/
│   ├── auth.js             # Funções de requisição REST para o Neon Auth
│   └── screens/
│       ├── HomeScreen.js    # Área logada com dados do usuário e logout
│       ├── LoginScreen.js   # Formulário de login
│       └── RegisterScreen.js# Formulário de cadastro
├── .env                     # Variável EXPO_PUBLIC_NEON_AUTH_URL
├── App.js                   # Roteamento por máquina de estados e checagem de sessão
├── package.json
└── README.md
```

## Como Executar

1. Clone o repositório:
```bash
git clone https://github.com/uriLopes/meu-app-auth.git
cd meu-app-auth
```

2. Instale as dependências:
```bash
npm install
```

3. Configure o arquivo `.env`:
```env
EXPO_PUBLIC_NEON_AUTH_URL=https://ep-dry-water-bdgd9qah.neonauth.c-8.us-east-2.aws.neon.tech/neondb/auth
```

4. Inicie o servidor Expo:
```bash
npx expo start
```
- Pressione `w` para abrir no navegador.
- Ou escaneie o QR Code com o aplicativo **Expo Go** no celular.
