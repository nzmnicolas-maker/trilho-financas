# Trilho — Controle Financeiro CLT

App web único (HTML/CSS/JS, sem build, sem backend) para controlar gastos e acompanhar rendimentos com base no calendário de pagamento CLT.

## Funcionalidades

- Cálculo automático da data de pagamento (dia-base configurável, padrão dia 2) com ajuste para o próximo dia útil quando cai em fim de semana.
- Painel de saldo do mês com indicador visual: **verde** = rendimento positivo, **vermelho** = gastos acima da renda.
- Gráfico de fluxo mensal (3 meses anteriores + atual + 2 futuros, com previsão em destaque dourado).
- Lançamento rápido de gastos e rendas extras, por categoria e data.
- Lista dos próximos pagamentos já com a data real de crédito.
- Dados salvos localmente no aparelho (`localStorage`) — nenhum dado sai do seu navegador.
- Preparado para uso como app no iOS (Adicionar à Tela de Início, tela cheia, ícone próprio).

## Como publicar no GitHub Pages

1. Crie um repositório novo no GitHub (ex: `trilho-financas`).
2. Suba o arquivo `index.html` (e este `README.md`) para a branch `main`.
3. No repositório, vá em **Settings → Pages**.
4. Em "Source", selecione a branch `main` e a pasta `/ (root)`. Salve.
5. Aguarde alguns segundos e acesse o link gerado, algo como:
   `https://SEU-USUARIO.github.io/trilho-financas/`

## Como usar no iPhone (iOS)

1. Abra o link do GitHub Pages no **Safari**.
2. Toque no ícone de compartilhar (quadrado com seta para cima).
3. Escolha **"Adicionar à Tela de Início"**.
4. O app abrirá em tela cheia, com ícone próprio, como um aplicativo nativo.

## Configuração inicial

Ao abrir o app pela primeira vez, toque no ícone de engrenagem (canto superior direito) e ajuste:

- **Salário líquido**: valor recebido por mês (padrão R$ 1.500).
- **Dia base do pagamento**: dia do mês em que o salário costuma cair (padrão dia 2).

A partir daí, basta usar o botão **+** para lançar gastos ou rendas extras. O app recalcula o saldo, o gráfico e as previsões automaticamente.

## Privacidade

Não há servidor, banco de dados externo ou coleta de dados. Tudo é armazenado apenas no `localStorage` do navegador em que o app for aberto. Isso significa que, se você trocar de aparelho ou apagar os dados do Safari, o histórico local será perdido — não há sincronização entre dispositivos nesta versão.

## Estrutura

```
trilho-financas/
├── index.html   → aplicativo completo (HTML + CSS + JS)
└── README.md    → este arquivo
```

## Possíveis evoluções futuras

- Sincronização em nuvem (ex: Firebase) para acessar de vários aparelhos.
- Exportar histórico em CSV/PDF.
- Metas de economia mensal.
- Notificações push de pagamento (exige um wrapper nativo ou PWA com service worker).
