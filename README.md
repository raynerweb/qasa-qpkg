# Qasa para QNAP

Repositório de aplicativos do **Qasa** para o App Center do QTS. Aqui ficam só o pacote
(`.qpkg`), os ícones e o `repo.xml`; o código-fonte do Qasa não é público.

O Qasa é um serviço que roda no NAS (no Container Station) e serve as fotos para o app no
telefone, em casa ou fora. Ele lê as fotos **somente leitura** e guarda o próprio índice numa
pasta separada. Desinstalar não apaga fotos nem essa pasta.

## Requisitos

- NAS QNAP x86_64 (Intel/AMD) com QTS 5.0 ou mais novo
- Container Station 3 instalado e ligado

## Instalar pelo repositório

1. App Center > Configurações > Geral: permitir a instalação de apps sem assinatura digital.
2. App Center > Configurações > Repositório de aplicativos > Adicionar:
   - Nome: `Qasa`
   - URL: `https://raynerweb.github.io/qasa-qpkg/repo.xml`
3. O Qasa aparece no App Center; instale e atualize por lá.

## Instalar manualmente

Baixe o `.qpkg` em [Releases](https://github.com/raynerweb/qasa-qpkg/releases), confira o
`.sha256` e use o botão de instalação manual do App Center.

## Depois de instalar

O serviço responde na porta 8090. Os caminhos ficam em `.qpkg/Qasa/qasa.conf`:

| Chave | Padrão |
|---|---|
| `QASA_MEDIA_DIR` | `/share/Multimedia/cameras` (somente leitura) |
| `QASA_DATA_DIR` | `/share/Container/qasa-server/data` |
| `QASA_PORT` | `8090` |

Nenhuma conta vem no pacote. Crie as contas pelo terminal do NAS:

```
docker exec -it qasa-server /opt/qasa-server/bin/qasa-server user add <nome> <pasta> [--child]
docker exec -it qasa-server /opt/qasa-server/bin/qasa-server user password <nome>
```
