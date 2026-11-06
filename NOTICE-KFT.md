# KFT Suporte: aviso de modificações

Este repositório é um fork do [RustDesk](https://github.com/rustdesk/rustdesk), Copyright © Purslane Tech Pte. Ltd., distribuído sob a **GNU Affero General Public License v3.0** (arquivo `LICENCE`). O KFT Suporte continua sob a mesma licença e é distribuído **sem garantia**.

- **Base:** RustDesk 1.5.1 (tag `1.5.1`, commit `23e5bb471a040d62f0a6ad52591fb30784265b73`), submódulo `hbb_common` em `fae47e024dd83cef6aaecde0aa7d11731df11649`.
- **Branch:** `kft-1.5.1`.
- **Modificado por:** KFT Triade, em 06/11/2026.

## O que foi modificado

| Arquivo | Mudança |
|---|---|
| `kft/custom.json` (novo) | Configuração do cliente: nome "KFT Suporte", só recebe conexões, sem instalação, servidor e chave próprios, aceite por clique, só senha temporária, configurações de servidor, rede e segurança ocultas. |
| `src/common.rs` | `load_custom_client()` e `read_custom_client()` passam a aplicar **somente** a configuração embutida (`include_bytes!`). Foram removidas a leitura de `custom.txt` externo e a verificação de assinatura da RustDesk. |
| `.github/workflows/kft-windows.yml` (novo) | Build manual Windows x64 portátil. No submódulo `hbb_common`, troca o servidor público padrão (`rs-ny.rustdesk.com`) e a chave padrão pelo servidor KFT. Inclui verificações que falham o build. |
| `Cargo.toml`, `libs/portable/Cargo.toml`, `flutter/windows/runner/Runner.rc` | Nome do produto, descrição e copyright (mantém o da Purslane e acrescenta as modificações da KFT). |
| `res/*.png`, `res/*.ico`, `flutter/windows/runner/resources/app_icon.ico`, `flutter/assets/icon.png`, `flutter/assets/logo.png`, `flutter/assets/logo_dark.png` | Ícones e logo da KFT (provisórios na primeira versão). |

O nome e o logo "RustDesk" pertencem aos seus titulares. O KFT Suporte não é um produto da RustDesk nem da Purslane Tech. A menção "Powered by RustDesk" no app é atribuição.

## Código-fonte

O código-fonte completo de cada versão distribuída fica neste repositório, na tag correspondente ao build (ex.: `kft-1.5.1-1`).
