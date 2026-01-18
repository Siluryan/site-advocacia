# Deploy no Firebase

## Passos para Deploy

### 1. Instalar Firebase CLI
```bash
sudo npm install -g firebase-tools
```

### 2. Fazer Login
```bash
firebase login
```

### 3. Criar Projeto no Firebase Console
1. Acesse: https://console.firebase.google.com/
2. Clique em "Adicionar projeto"
3. Use o ID: `advogadoemmarilia` (ou outro de sua escolha)
4. Anote o ID do projeto criado

### 4. Configurar Projeto
Edite o arquivo `.firebaserc` e altere o ID do projeto se necessário:
```json
{
  "projects": {
    "default": "advogadoemmarilia"
  }
}
```

### 5. Inicializar Firebase Hosting (primeira vez)
```bash
firebase init hosting
```
- Selecione "Use an existing project"
- Escolha o projeto `advogadoemmarilia`
- Diretório público: `.` (ponto)
- Single-page app: **Sim**
- Não sobrescrever index.html: **Não**

### 6. Fazer Deploy
```bash
firebase deploy --only hosting
```

## Site Publicado

Após o deploy, o site estará disponível em:
- https://advogadoemmarilia.web.app
- https://advogadoemmarilia.firebaseapp.com

## Atualizar Site

Após fazer alterações nos arquivos:
```bash
firebase deploy --only hosting
```
