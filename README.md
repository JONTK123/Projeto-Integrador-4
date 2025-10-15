# GoCampus 🚌📚

<div align="center">
  <img src="assets/logo_go_campus.png" alt="GoCampus Logo" width="200"/>
  
  [![Flutter](https://img.shields.io/badge/Flutter-SDK%203.5.3%2B-02569B?logo=flutter)](https://flutter.dev)
  [![Firebase](https://img.shields.io/badge/Firebase-Enabled-FFA611?logo=firebase)](https://firebase.google.com)
  [![License](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)
</div>

## 📋 Sobre o Projeto

O **GoCampus** é uma plataforma inovadora que conecta estudantes a empresas de transporte universitário de forma prática e eficiente. Com o GoCampus, os usuários podem buscar por empresas que oferecem serviços de transporte para suas universidades ou regiões, avaliar essas empresas e escolher a melhor opção para suas necessidades. As empresas, por sua vez, podem se cadastrar na plataforma, fornecer informações sobre suas rotas e atrair mais clientes.

### 🎯 Objetivo

Facilitar a conexão entre estudantes e empresas de transporte universitário, promovendo transparência através de avaliações e oferecendo uma experiência intuitiva e moderna para ambos os lados.

## ✨ Funcionalidades

### 👨‍🎓 Para Usuários (Estudantes)
- 🔍 **Busca Inteligente**: Encontre empresas de transporte que atendem à sua universidade ou região
- ⭐ **Avaliações e Comentários**: Deixe sua avaliação e compartilhe sua experiência com as empresas
- 🎨 **Filtros Personalizados**: Filtre empresas por cidade de partida e instituição de destino
- 🗺️ **Rotas Disponíveis**: Visualize todas as rotas oferecidas pelas empresas
- 📱 **Interface Intuitiva**: Design moderno e fácil de usar
- 🔐 **Login Seguro**: Autenticação via Firebase para proteger seus dados
- 💾 **Dados Salvos**: Suas preferências são salvas automaticamente

### 🏢 Para Empresas
- 📝 **Cadastro Completo**: Cadastre sua empresa com todas as informações necessárias (CNPJ, telefone, endereço)
- 🛣️ **Gerenciamento de Rotas**: Adicione, edite e remova rotas de forma simples
- 📊 **Feedback dos Usuários**: Receba avaliações e comentários para melhorar seus serviços
- 👁️ **Visibilidade**: Aumente sua presença e atraia novos clientes
- ✏️ **Perfil Editável**: Atualize as informações da sua empresa a qualquer momento

## 🛠️ Tecnologias Utilizadas

### Frontend
- **[Flutter](https://flutter.dev)** - Framework multiplataforma para desenvolvimento mobile
- **[Dart](https://dart.dev)** - Linguagem de programação

### Principais Dependências
```yaml
dependencies:
  firebase_core: ^3.6.0          # Integração com Firebase
  firebase_auth: ^5.3.1          # Autenticação de usuários
  http: ^1.2.2                    # Requisições HTTP para API
  shared_preferences: ^2.0.15     # Armazenamento local
  flutter_rating_bar: ^4.0.1      # Sistema de avaliação
  flutter_masked_text2: ^0.9.0    # Máscaras para campos de texto
  intl: ^0.19.0                   # Internacionalização
```

### Backend
- **Java** - Backend API para gerenciamento de dados
- **MongoDB** - Banco de dados NoSQL para armazenamento de informações

### Serviços
- **Firebase Authentication** - Autenticação segura de usuários
- **Firebase Core** - Configuração base do Firebase

## 📱 Estrutura do Aplicativo

```
lib/
├── main.dart                          # Ponto de entrada do app
├── splash_screen.dart                 # Tela de abertura
├── login_screen.dart                  # Tela de login
├── register_screen.dart               # Tela de cadastro
├── search_screen.dart                 # Tela de busca (usuários)
├── company_screen.dart                # Tela da empresa (gestão)
├── company_details_screen.dart        # Detalhes e avaliação da empresa
├── company_evaluation_screen.dart     # Sistema de avaliação
├── firebase_options.dart              # Configurações do Firebase
└── services/
    ├── auth_service.dart              # Serviço de autenticação
    ├── register_service.dart          # Serviço de registro e API
    └── date_picker_service.dart       # Serviço de seleção de data
```

## 🚀 Como Executar o Projeto

### Pré-requisitos

Antes de começar, certifique-se de ter as seguintes ferramentas instaladas:

- ✅ **Flutter SDK** (3.5.3 ou superior)
- ✅ **Dart SDK** (3.5.3 ou superior)
- ✅ **Android Studio** ou **VS Code** com extensões Flutter/Dart
- ✅ **Git** para controle de versão
- ✅ **Java JDK** (para o backend)
- ✅ **MongoDB** instalado e rodando
- ✅ Conta no **Firebase** configurada

### 📥 Instalação

#### 1. Clone o repositório

```bash
git clone https://github.com/JONTK123/Projeto-Integrador-4.git
cd Projeto-Integrador-4
```

#### 2. Instale as dependências do Flutter

```bash
flutter pub get
```

#### 3. Configure o Firebase

O projeto já está configurado com Firebase. Certifique-se de que:
- O arquivo `lib/firebase_options.dart` existe
- O arquivo `android/app/google-services.json` está presente (para Android)
- As configurações no `firebase.json` estão corretas

Se precisar reconfigurar:

```bash
# Instale o Firebase CLI
npm install -g firebase-tools

# Faça login no Firebase
firebase login

# Configure o projeto
flutterfire configure
```

#### 4. Configure o Backend

Certifique-se de que o backend Java está rodando e conectado ao MongoDB. O app se comunica com o backend através de requisições HTTP definidas em `lib/services/register_service.dart`.

#### 5. Execute o aplicativo

Para Android:
```bash
flutter run
```

Para iOS:
```bash
flutter run -d ios
```

Para Web:
```bash
flutter run -d chrome
```

### 🔧 Configuração Adicional

#### Variáveis de Ambiente

Certifique-se de configurar corretamente:
- URL da API do backend no arquivo `register_service.dart`
- Credenciais do Firebase
- Configurações do MongoDB no backend

#### Resolução de Problemas Comuns

**Problema: Erro ao executar `flutter pub get`**
```bash
# Limpe o cache e tente novamente
flutter clean
flutter pub get
```

**Problema: Firebase não inicializa**
```bash
# Verifique se o Firebase está configurado corretamente
flutterfire configure
```

**Problema: Erro de build no Android**
```bash
# Limpe o build do Android
cd android
./gradlew clean
cd ..
flutter clean
flutter pub get
```

## 📸 Capturas de Tela

<!-- Adicione capturas de tela do aplicativo aqui -->
_Em breve: capturas de tela das principais funcionalidades_

## 🏗️ Arquitetura do Projeto

O projeto segue uma arquitetura em camadas:

- **Camada de Apresentação**: Screens (UI/UX em Flutter)
- **Camada de Serviços**: Services (Lógica de negócio e comunicação com APIs)
- **Camada de Backend**: API Java + MongoDB
- **Camada de Autenticação**: Firebase Authentication

```
┌─────────────────┐
│   Flutter App   │
│   (Frontend)    │
└────────┬────────┘
         │
         ├──────────────┐
         │              │
┌────────▼────────┐ ┌──▼──────────┐
│ Firebase Auth   │ │  Backend    │
│                 │ │  Java API   │
└─────────────────┘ └──────┬──────┘
                           │
                    ┌──────▼──────┐
                    │  MongoDB    │
                    └─────────────┘
```

## 🔌 Endpoints da API

O aplicativo se comunica com o backend através dos seguintes endpoints:

### Empresas
- `POST /empresa` - Cadastrar nova empresa
- `GET /empresa` - Buscar empresas por trajeto
- `PUT /empresa` - Atualizar dados da empresa

### Usuários
- `POST /usuario` - Cadastrar novo usuário
- `GET /usuario` - Obter dados do usuário

### Trajetos
- `POST /trajeto` - Adicionar novo trajeto
- `GET /trajeto` - Listar trajetos

### Avaliações
- `POST /avaliacao` - Adicionar avaliação
- `GET /avaliacao` - Obter avaliações de uma empresa

## 🧪 Testes

Para executar os testes:

```bash
# Executar todos os testes
flutter test

# Executar testes com cobertura
flutter test --coverage
```

## 🚢 Deploy

### Android (APK/AAB)

```bash
# Gerar APK
flutter build apk --release

# Gerar App Bundle (para Google Play Store)
flutter build appbundle --release
```

### iOS

```bash
# Gerar IPA
flutter build ios --release
```

### Web

```bash
# Build para web
flutter build web
```

## 🤝 Como Contribuir

Contribuições são sempre bem-vindas! Para contribuir:

1. Faça um Fork do projeto
2. Crie uma branch para sua feature (`git checkout -b feature/NovaFuncionalidade`)
3. Commit suas mudanças (`git commit -m 'Adiciona nova funcionalidade'`)
4. Push para a branch (`git push origin feature/NovaFuncionalidade`)
5. Abra um Pull Request

### 📝 Padrões de Código

- Siga as convenções de código do Dart/Flutter
- Use nomes descritivos para variáveis e funções
- Comente código complexo quando necessário
- Mantenha funções pequenas e com responsabilidade única

## 📄 Licença

Este projeto está sob a licença MIT. Veja o arquivo [LICENSE](LICENSE) para mais detalhes.

## 👥 Equipe

Desenvolvido como Projeto Integrador 4

## 📞 Contato

Para dúvidas, sugestões ou feedback:

- 🐛 Issues: [GitHub Issues](https://github.com/JONTK123/Projeto-Integrador-4/issues)
- 💬 Discussões: [GitHub Discussions](https://github.com/JONTK123/Projeto-Integrador-4/discussions)

## 🗺️ Roadmap

### ✅ Implementado
- Sistema de autenticação com Firebase
- Cadastro de usuários e empresas
- Busca de empresas por trajeto
- Sistema de avaliações
- Gerenciamento de rotas

### 🔜 Próximas Funcionalidades
- [ ] Sistema de notificações push
- [ ] Chat entre usuários e empresas
- [ ] Integração com mapas (Google Maps)
- [ ] Sistema de pagamento integrado
- [ ] Agendamento de viagens
- [ ] Histórico de viagens
- [ ] Modo escuro
- [ ] Suporte a múltiplos idiomas
- [ ] Dashboard analítico para empresas

## 📊 Status do Projeto

🟢 **Ativo** - Em desenvolvimento contínuo

---

<div align="center">
  Feito com ❤️ pela equipe GoCampus
  
  ⭐ Se este projeto te ajudou, considere dar uma estrela!
</div>