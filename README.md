# 📦 TransferTool — Downloads Oficiais

[![Latest release](https://img.shields.io/github/v/release/VitorRosaDev/TransferToolReleases?style=for-the-badge&logo=github&label=release)](https://github.com/VitorRosaDev/TransferToolReleases/releases)
[![Platform](https://img.shields.io/badge/Plataforma-Android%20%C2%B7%20Windows-blue?style=for-the-badge)](https://github.com/VitorRosaDev/TransferToolReleases/releases)
[![License](https://img.shields.io/badge/Licen%C3%A7a-LGPLv3-orange?style=for-the-badge)](LICENSE)

Este repositório é o **ponto único de distribuição** dos instaladores oficiais do
ecossistema **TransferTool** — a ferramenta de logística **offline-first** criada
para o **Almoxarifado Central Municipal**.

> 🔒 O **código-fonte é privado**. Aqui publicamos **apenas os binários**
> e as notas de versão, para que qualquer pessoa possa instalar as aplicações sem
> depender de loja de aplicativos.

---

## ⬇️ Download

| Aplicação                | Plataforma | Arquivo                           | Download                                                                                                                            |
| :----------------------- | :--------- | :-------------------------------- | :---------------------------------------------------------------------------------------------------------------------------------- |
| **TransferTool Mobile**  | Android    | `TransferTool-1.2.0.apk`          | [Baixar](https://github.com/VitorRosaDev/TransferToolReleases/releases/download/v1.2.0/TransferTool-1.2.0.apk)                        |
| **TransferTool RPA**     | Windows    | `TransferToolRPA-Setup-1.2.0.exe` | [Baixar](https://github.com/VitorRosaDev/TransferToolReleases/releases/download/v1.2.0/TransferToolRPA-Setup-1.2.0.exe)              |

📚 **Todas as versões e notas de lançamento:** [Releases](https://github.com/VitorRosaDev/TransferToolReleases/releases)

---

## 📱 TransferTool Mobile — o que é

Um **coletor de dados inteligente** que organiza a conferência e a distribuição
de mantimentos (rancho escolar e materiais de consumo) entre o depósito central
e as escolas da rede municipal — **sem precisar de internet**.

O operador monta as cargas no depósito, faz a conferência física, consolida e, ao
final, exporta um arquivo que o escritório automatiza para dentro do ERP. Nada é
digitado duas vezes.

### ✨ Principais recursos

- **100% offline** — funciona em qualquer galpão, mesmo sem sinal.
- **Montagem em 3 passos** — Rota → Origem → Destino, com criação de rota na hora.
- **Catálogo próprio** — itens, depósitos e escolas com busca por código ou nome.
- **Itens fracionados** — registra em pacotes e converte automaticamente para kg no envio.
- **Depósito vinculado** — a busca de itens na carga mostra apenas o que pertence ao depósito certo.
- **Área de transferência por rota** — as cargas se agrupam por rota, mais antigas primeiro.
- **Ciclo de vida com segurança** — `Rascunho → Consolidada → Exportada`, com reabertura para correção.
- **Exportação por rota** — um arquivo JSON por rota, pronto para automação (RPA) no ERP.

---

## 🔧 Como instalar (Android)

O aplicativo é distribuído como **APK assinado**, para instalação direta:

1. Baixe o arquivo `TransferTool-<versão>.apk` na página de [Releases](https://github.com/VitorRosaDev/TransferToolReleases/releases).
2. Abra o arquivo baixado no celular.
3. Se o Android solicitar, autorize **“Instalar apps desconhecidos”** para o app de onde
   o download foi feito (navegador ou gerenciador de arquivos).
4. Confirme a instalação e abra o **TransferTool**.

> ℹ️ **Requisitos:** Android 8.0 ou superior e cerca de 150 MB de espaço livre.
> O aparelho **não precisa de internet** para operar.

> ⚠️ **Atualização:** ao instalar uma versão mais nova por cima, os dados locais são
> preservados. Não é necessário desinstalar antes.

---

## 🔄 Como funciona (visão do operador)

1. **Montar carga** — escolha a **Rota**, o **Depósito** de origem e a **Escola** de destino.
2. **Adicionar itens** — busque pelo código ou pelo nome; a sugestão já vem filtrada pelo
   depósito da carga. Informe a quantidade (em pacotes, para itens fracionados).
3. **Conferir e consolidar** — ao fechar a carga, o status passa para **Consolidada** e o
   conteúdo fica bloqueado para edição.
4. **Exportar** — selecione as rotas e gere um arquivo **JSON por rota**; em seguida o app
   pergunta se deseja remover as rotas já exportadas.
5. **Automatizar** — o arquivo é consumido pelo **TransferTool RPA**, que preenche o ERP.

---

## 🖥️ TransferTool RPA (Windows) — o que é

O **par desktop** do TransferTool: um robô de automação (**RPA**) que lê os
arquivos JSON exportados pelo aplicativo Mobile e **preenche automaticamente o
ERP** da prefeitura, eliminando a digitação manual das transferências.

Enquanto o Mobile coleta as cargas no depósito (offline), o RPA faz o lançamento
no escritório — os dois lados nunca digitam o mesmo dado duas vezes.

### ✨ Principais recursos

- **Preenchimento automático no ERP** — importa o JSON e executa a transferência tela a tela.
- **Fila sequencial** — várias cargas processadas em ordem, com status individual por carga.
- **Agrupamento por rota** — fila organizada em **Rota → Origem → cargas**, com os botões **Remover rota** e **Limpar seção**.
- **Log em tempo real** — cada passo (sucesso, aviso, erro) aparece no painel e é gravado em arquivo para rastreabilidade.
- **100% local** — a automação roda inteiramente no computador do escritório; nenhum dado é enviado a terceiros.

---

## 🔧 Como instalar (Windows)

O aplicativo é distribuído como **instalador único**
(`TransferToolRPA-Setup-<versão>.exe`), para instalação direta — **sem loja de aplicativos**:

1. Baixe o arquivo `TransferToolRPA-Setup-<versão>.exe` na página de [Releases](https://github.com/VitorRosaDev/TransferToolReleases/releases).
2. Execute o instalador — ele cria atalhos na **Área de Trabalho** e no **Menu Iniciar**.
3. Se o Windows exibir o aviso do **SmartScreen** ("O Windows protegeu o computador"),
   clique em **Mais informações → Executar assim mesmo**.
4. Abra o **TransferTool RPA** pelo atalho criado.

> ℹ️ **Requisitos:** Windows 10/11 (64 bits) e cerca de 600 MB de espaço livre.
> O instalador já embute o runtime .NET, o driver `node.exe` e os navegadores do
> Playwright — **não** é necessário instalar mais nada.

> ⚠️ **Assinatura:** o instalador usa um **certificado autoassinado**. Por isso o
> Windows pode avisar que o editor é desconhecido — o mesmo comportamento de
> qualquer software distribuído fora de uma loja. Baixe **sempre** por este
> repositório oficial.

---

## 🔄 Como funciona (visão do operador — Windows)

1. **Abrir o navegador** — no TransferTool RPA, clique em **🌐 Abrir Chrome**; o navegador
   abre já com a depuração habilitada, na tela de login do ERP.
2. **Fazer login manualmente** no sistema do ERP.
3. **Importar** — arraste o **arquivo JSON** exportado pelo TransferTool Mobile para a
   área de *drag-and-drop* do RPA.
4. **Iniciar RPA** — as cargas da fila são executadas em sequência, com o log mostrando
   o resultado de cada item (ok, parcial ou não encontrado).

---

## 🔐 Privacidade e LGPD

- **Mobile:** os dados ficam **no próprio dispositivo** (banco SQLite local) — sem servidores e sem envio a terceiros.
- **RPA (Windows):** a automação roda inteiramente no computador do escritório; os arquivos JSON não são transmitidos a terceiros.
- Não há coleta de telemetria nem necessidade de login próprio.
- Ao desinstalar o aplicativo Mobile, o banco local é removido.

---

## 🏗️ Especificações técnicas (resumo)

### TransferTool Mobile

- **Aplicativo:** React Native + Expo (TypeScript), empacotado com EAS Build.
- **Armazenamento:** SQLite local **offline-first**, com integridade referencial e modo WAL.
- **Sem backend:** a sincronização acontece por **arquivos de exportação JSON**, consumidos
  pela automação RPA do escritório.
- **Distribuição:** APK **assinado** gerado na nuvem; o certificado de assinatura é
  gerenciado pelo Expo (EAS) e nunca é versionado.
- **Plataforma:** Android (builds de homologação via perfil interno do EAS).

### TransferTool RPA (Windows)

- **Aplicativo:** C# / **.NET 8** com **WPF**, sob **Clean Architecture + Clean MVVM** e Command Pattern.
- **Automação:** **Microsoft Playwright** conectado ao navegador via **CDP** (Chrome DevTools Protocol, restrito a `127.0.0.1:9222`) — o RPA opera sobre um Chrome já aberto pelo operador, na sessão autenticada.
- **Sem backend:** consome os **arquivos JSON** exportados pelo Mobile; nada é enviado a servidores externos.
- **Distribuição:** instalador **Inno Setup** self-contained (embute o runtime .NET e os navegadores do Playwright); assinado com **certificado autoassinado**.
- **Plataforma:** Windows 10/11 (64 bits).

---

## 🗂️ Notas de versão

O histórico completo fica na aba **[Releases](https://github.com/VitorRosaDev/TransferToolReleases/releases)**.
Cada versão segue [Versionamento Semântico](https://semver.org/lang/pt-BR/) e é publicada
com os binários anexados — `TransferTool-<versão>.apk` (Android) e
`TransferToolRPA-Setup-<versão>.exe` (Windows).

---

## ❓ Perguntas frequentes

**O aplicativo precisa de internet?**
Não. Todo o fluxo — cadastro, montagem, conferência e exportação — acontece offline.

**Por que o Android avisa sobre “fonte desconhecida”?**
Porque o app é distribuído fora da Play Store, como APK assinado. É o mesmo
comportamento de qualquer instalação direta.

**Perco meus dados ao atualizar?**
Não. A atualização substitui o aplicativo e mantém o banco local.

**Onde ficam os dados exportados?**
No armazenamento do aparelho, de onde podem ser compartilhados com o escritório.

**Por que o Windows avisa que o editor é desconhecido?**
Porque o instalador do RPA usa um **certificado autoassinado**, comum em software
distribuído fora de uma loja. Baixe **sempre** por este repositório oficial e prossiga em
**Mais informações → Executar assim mesmo**.

**Preciso usar as duas aplicações juntas?**
Elas se completam: o **Mobile** coleta as cargas no depósito (offline) e o **RPA** lança os
JSONs no ERP do escritório. É possível usar apenas uma delas, conforme a rotina.

**O RPA precisa de internet?**
Sim — ele acessa o ERP web da prefeitura. A coleta no **Mobile**, porém, é 100% offline.

---

## 📄 Licença

Distribuído sob a licença [GNU Lesser General Public License v3.0](LICENSE) (LGPLv3).

---

*Gerenciado e desenvolvido por **Vitor Rodrigues da Rosa** — Projeto TransferTool — 2026*

