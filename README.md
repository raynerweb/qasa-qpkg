# Qasa: pacote do NAS

> **App independente.** O Qasa é um projeto pessoal e independente, feito por raynerweb. **Não é um produto da
> QNAP** e não é desenvolvido, mantido, verificado nem apoiado pela QNAP Systems, Inc. QNAP, QTS e App Center são
> marcas da QNAP Systems, Inc. e aparecem aqui só para dizer em quais aparelhos o Qasa funciona.
>
> *Independent app: Qasa is a personal project by raynerweb. It is not a QNAP product and is not developed,
> maintained, verified or endorsed by QNAP Systems, Inc. — [English instructions](https://raynerweb.github.io/qasa-qpkg/#en).*

Página com o passo a passo: **https://raynerweb.github.io/qasa-qpkg/**

Aqui ficam só o pacote do NAS (`.qpkg`, nas [Releases](https://github.com/raynerweb/qasa-qpkg/releases)), os
ícones, o `repo.xml` e as páginas públicas (instalação, conexão por QR e privacidade). O código-fonte do Qasa não é
público.

O Qasa é um serviço que roda no NAS (no Container Station) e serve as fotos para o app no telefone, em casa ou
fora. Ele lê as fotos **somente leitura** e guarda o próprio índice numa pasta separada. Desinstalar não apaga
fotos nem essa pasta.

## Requisitos

- NAS QNAP x86_64 (Intel/AMD) com QTS 5.0 ou mais novo
- Container Station 3 instalado e ligado

## Instalar (instalação manual)

O Qasa não está na loja oficial do App Center; a instalação é manual.

1. Baixe o `.qpkg` e o `.sha256` da [versão mais recente](https://github.com/raynerweb/qasa-qpkg/releases/latest)
   e confira o arquivo (`shasum -a 256 Qasa_*_x86_64.qpkg` no Mac/Linux,
   `certutil -hashfile <arquivo> SHA256` no Windows).
2. App Center > Configurações > Geral: permitir a instalação de apps sem assinatura digital (o pacote não é
   assinado pela QNAP).
3. App Center > botão de instalação manual > escolher o `.qpkg`.
4. Abrir o ícone do Qasa no QTS: o assistente cria as contas da família e o QR code de cada telefone.

### Atualizações automáticas (opcional)

App Center > Configurações > Repositório de aplicativos > Adicionar:

- Nome: `Qasa`
- URL: `https://raynerweb.github.io/qasa-qpkg/repo.xml`

Este repositório é mantido por raynerweb, não pela QNAP.

## Depois de instalar

O serviço responde na porta 8090. Os caminhos ficam em `.qpkg/Qasa/qasa.conf`:

| Chave | Padrão |
|---|---|
| `QASA_MEDIA_DIR` | `/share/Multimedia/cameras` (somente leitura) |
| `QASA_DATA_DIR` | `/share/Container/qasa-server/data` |
| `QASA_PORT` | `8090` |

Nenhuma conta vem no pacote: crie as contas da família no assistente (ícone do Qasa no QTS).

## Segurança

Problemas de segurança: escreva para **raynerweb.apps@gmail.com** e não abra uma questão pública. Detalhes em
[SECURITY.md](SECURITY.md).

## Dúvidas e problemas

Abra uma questão em [Issues](https://github.com/raynerweb/qasa-qpkg/issues). Não peça suporte do Qasa à QNAP:
eles não fazem nem mantêm este app.
