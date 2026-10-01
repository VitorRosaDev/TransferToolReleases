# 📦 TransferTool — Downloads Oficiais

[![Latest release](https://img.shields.io/github/v/release/VitorRosaDev/TransferToolReleases?style=for-the-badge&logo=github&label=release)](https://github.com/VitorRosaDev/TransferToolReleases/releases)
[![Platform](https://img.shields.io/badge/Plataforma-Android%20%C2%B7%20Windows-blue?style=for-the-badge)](https://github.com/VitorRosaDev/TransferToolReleases/releases)
[![License](https://img.shields.io/badge/Licen%C3%A7a-LGPLv3-orange?style=for-the-badge)](LICENSE)

Este repositório é o **ponto único de distribuição** dos instaladores oficiais do
ecossistema **TransferTool** — a ferramenta de logística **offline-first** criada
para o **Almoxarifado Central Municipal**.

> 🔒 O **código-fonte é privado**. Aqui publicamos **apenas os binários assinados**
> e as notas de versão, para que os coletores possam instalar o aplicativo sem
> depender de loja de aplicativos.

---

## ⬇️ Download

| Aplicação                | Plataforma | Arquivo                  | Download                                                                                                        |
| :----------------------- | :--------- | :----------------------- | :-------------------------------------------------------------------------------------------------------------- |
| **TransferTool Mobile**  | Android    | `TransferTool-1.2.0.apk` | [Baixar](https://github.com/VitorRosaDev/TransferToolReleases/releases/download/v1.2.0/TransferTool-1.2.0.apk)   |

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

## 🔐 Privacidade e LGPD

- Os dados ficam **no próprio dispositivo** (banco SQLite local) — **sem servidores** e sem
  envio a terceiros.
- Não há coleta de telemetria nem necessidade de login.
- Ao desinstalar o app, o banco local é removido.

---

## 🏗️ Especificações técnicas (resumo)

- **Aplicativo:** React Native + Expo (TypeScript), empacotado com EAS Build.
- **Armazenamento:** SQLite local **offline-first**, com integridade referencial e modo WAL.
- **Sem backend:** a sincronização acontece por **arquivos de exportação JSON**, consumidos
  pela automação RPA do escritório.
- **Distribuição:** APK **assinado** gerado na nuvem; o certificado de assinatura é
  gerenciado pelo Expo (EAS) e nunca é versionado.
- **Plataforma:** Android (builds de homologação via perfil interno do EAS).

---

## 🗂️ Notas de versão

O histórico completo fica na aba **[Releases](https://github.com/VitorRosaDev/TransferToolReleases/releases)**.
Cada versão segue [Versionamento Semântico](https://semver.org/lang/pt-BR/) e é publicada
com o APK anexado (`TransferTool-<versão>.apk`).

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

---

## 📄 Licença

Distribuído sob a licença [GNU Lesser General Public License v3.0](LICENSE) (LGPLv3).

---

*Gerenciado e desenvolvido por **Vitor Rodrigues da Rosa** — Projeto TransferTool — 2026*

