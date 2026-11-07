# Finanças da Casa

App para controle financeiro da casa: entradas, saídas, forma de pagamento
(Pix, crédito, débito, dinheiro, boleto), contas fixas com vencimento e backup.
Funciona offline. Os dados ficam salvos no próprio aparelho.

Todo o app está em `www/index.html`.

---

## iPhone — Opção A: instalar pelo Safari (recomendado, grátis, sem Mac)
1. Envie esta pasta para um repositório no GitHub.
2. No repositório: **Settings → Pages → Source: GitHub Actions**.
3. Na aba **Actions**, rode "Publicar app web (iPhone)". Ele gera um link tipo
   `https://SEU-USUARIO.github.io/financas-casa/`.
4. No iPhone, abra o link no **Safari** → botão **Compartilhar** → **Adicionar à Tela de Início**.
5. Pronto: ícone na tela, abre em tela cheia e funciona sem internet.

> Os dados ficam no iPhone. Use **Ajustes → Exportar** de vez em quando
> (abre a folha de compartilhar: salve em Arquivos, iCloud ou WhatsApp).

## iPhone — Opção B: app nativo (precisa de um Mac com Xcode)
```bash
npm install
npm run ios        # cria a pasta ios/ e abre no Xcode
```
No Xcode: selecione o projeto **App** → **Signing & Capabilities** → escolha seu Apple ID
em *Team* → conecte o iPhone → ▶ Run.
- Com Apple ID grátis o app expira em 7 dias (é só rodar de novo).
- Para durar e publicar na App Store / TestFlight: Apple Developer Program (US$ 99/ano).
- Ícone de 1024px para o Xcode: `www/icons/icon-1024.png`.

---

## Android — gerar APK pelo GitHub
O workflow **Gerar APK** roda sozinho a cada envio. Na execução em **Actions**, baixe
**financas-casa-apk**, descompacte e instale o `app-debug.apk` no celular.

No computador (Android Studio): `npm install && npm run android && npm run apk`.

## Depois de mudar o app
`npx cap sync` e gere de novo.
