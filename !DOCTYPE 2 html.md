# Sistema de Denúncias Ambientais — BPAmb

Plataforma web moderna, responsiva e institucional desenvolvida para o **Batalhão de Policiamento Ambiental (BPAmb)**, destinada ao recebimento simplificado de denúncias de crimes e infrações ambientais pela população, bem como à gestão interna pelas equipes policiais.

---

## 🛠️ Tecnologias Utilizadas
- **HTML5 & Tailwind CSS:** Interface moderna, limpa, totalmente responsiva para smartphones e computadores, utilizando identidade visual verde institucional.
- **JavaScript (ES6+):** Gerenciamento de estado, validações de formulário, geração de protocolos e simulação de persistência.
- **FontAwesome:** Ícones institucionais de segurança e meio ambiente.

---

## 🚀 Como Publicar no GitHub Pages (Hospedagem Gratuita)

1. Crie um novo repositório público no GitHub (ex: `sistema-denuncias-bpamb`).
2. Faça o upload dos arquivos `index.html` e `README.md` na raiz do repositório.
3. No seu repositório, acesse a aba **Settings** (Configurações).
4. No menu lateral esquerdo, clique em **Pages**.
5. Em **Build and deployment**, na opção **Branch**, selecione `main` (ou `master`) e `/ (root)` e clique em **Save**.
6. Em poucos minutos, o GitHub fornecerá o link público de acesso ao sistema.

---

## 🔒 Funcionalidades Implementadas

### 1. Página Pública e Formulário do Cidadão
- **Design Institucional:** Cores baseadas em tons de verde, branco e cinzas neutros, destacando o nome do BPAmb.
- **Avisos de Segurança:** Alerta claro para o cidadão não se aproximar de suspeitos ou colocar sua integridade em risco.
- **Campos Diretos:** Seleção rápida do tipo de ocorrência (desmatamento, queimadas, poluição, fauna/flora, etc.), descrição, município, endereço e opção de anexar evidências.
- **Anonimato Destacado:** Checkbox que oculta e dispensa dados de identificação pessoal, garantindo total sigilo ao denunciante.

### 2. Geração de Protocolo e Consulta
- **Protocolo Automático:** Criação de código único (ex: `BPA-2026-XXXXX`) com data e hora exatas.
- **Opções de Cópia e Impressão:** Facilidade para o cidadão guardar o comprovante.
- **Aba de Consulta:** Permite ao cidadão verificar o status atual da denúncia utilizando apenas o número do protocolo.
- **Transparência Institucional:** O sistema deixa claro que o protocolo serve para acompanhamento e que o registro não substitui chamadas de emergência imediata (190).

### 3. Painel Administrativo Restrito (Área Policial)
- **Acesso Seguro:** Tela de login para policiais e analistas autorizados.
- **Gestão de Ocorrências:** Tabela com listagem de denúncias, filtros dinâmicos por protocolo, município e status.
- **Fluxo de Atendimento:** Capacidade de alterar o status da denúncia (`Recebida`, `Em análise`, `Encaminhada`, `Em atendimento`, `Concluída`).
- **Observações Internas:** Campo restrito para anotações de diligências e histórico operacional invisível ao denunciante.

---

## ⚙️ Diretrizes para Produção e Integração Futura

Para implantar este protótipo em ambiente de produção real com banco de dados persistente (PostgreSQL/MySQL) e API backend (Node.js/Python):

1. **Segurança de Servidor:** Implementar autenticação corporativa (OAuth2 / LDAP da corporação) no painel administrativo e proteção robusta contra CSRF e ataques de força bruta.
2. **Armazenamento de Anexos:** Configurar buckets seguros (ex: AWS S3 ou armazenamento interno cifrado) para que fotos e vídeos de denúncias ambientais jamais fiquem expostos publicamente.
3. **Integração com WhatsApp:** O formulário atual já coleta números de contato de forma opcional; a futura API do WhatsApp Business poderá disparar mensagens automáticas de confirmação de protocolo para o cidadão.

