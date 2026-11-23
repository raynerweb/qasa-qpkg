# Política de segurança / Security policy

> O Qasa é um app independente, feito por raynerweb. Não é um produto da QNAP.
> Qasa is an independent app by raynerweb. It is not a QNAP product.

## Português

### Como avisar de um problema de segurança

Escreva para **{{EMAIL_SEGURANCA}}** com:

- a versão do pacote do NAS e/ou do app (iPhone ou Android);
- o que acontece e como repetir o problema;
- o que alguém poderia fazer com isso (por exemplo: ver fotos de outra conta, entrar sem senha).

**Não abra uma questão pública** (issue) para problemas de segurança. Não mande fotos, senhas nem dados pessoais
de verdade: se precisar mostrar algo, use dados de exemplo.

### O que esperar

- Resposta de recebimento em até **7 dias**.
- Uma avaliação inicial em até **14 dias**, dizendo se o problema foi confirmado e o que será feito.
- A correção sai numa versão nova, publicada nas [Releases](https://github.com/raynerweb/qasa-qpkg/releases),
  com uma nota sobre o problema corrigido. Se quiser, seu nome entra nos agradecimentos.

O Qasa é mantido por uma pessoa só, no tempo livre; os prazos acima são o compromisso de boa-fé.

### Versões que recebem correções

Só a **versão mais recente** do pacote do NAS e dos apps. Atualize antes de reportar, se puder.

### Escopo

- Pacote do NAS (`Qasa_*.qpkg`): o serviço `qasa-server`, o assistente web e o ajudante do pacote.
- Apps Qasa para iPhone e Android.
- As páginas deste site (`raynerweb.github.io/qasa-qpkg`).

Fora do escopo: o QTS, o App Center, o Container Station e o Tailscale. Problemas neles devem ir para os
respectivos fabricantes.

## English

### How to report a security issue

Email **{{EMAIL_SEGURANCA}}** with:

- the NAS package and/or app version (iPhone or Android);
- what happens and how to reproduce it;
- what someone could do with it (for example: see another account's photos, sign in without a password).

**Please do not open a public issue** for security problems. Do not send real photos, passwords or personal data;
use sample data if you need to show something.

### What to expect

- Acknowledgement within **7 days**.
- An initial assessment within **14 days**, saying whether the issue is confirmed and what will be done.
- The fix ships in a new version on [Releases](https://github.com/raynerweb/qasa-qpkg/releases), with a note about
  the fixed issue. You will be credited if you wish.

Qasa is maintained by one person in their spare time; these timelines are a good-faith commitment.

### Supported versions

Only the **latest version** of the NAS package and of the apps. Please update before reporting, if you can.

### Scope

- NAS package (`Qasa_*.qpkg`): the `qasa-server` service, the web setup assistant and the package helper.
- Qasa apps for iPhone and Android.
- The pages of this site (`raynerweb.github.io/qasa-qpkg`).

Out of scope: QTS, App Center, Container Station and Tailscale. Please report issues in those to their vendors.
