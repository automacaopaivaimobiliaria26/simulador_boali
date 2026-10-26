# Simulador Boali — pacote de publicação v8

Versão responsiva com as novas premissas iniciais e ajustes nos cálculos do mês de estabilização, ponto de equilíbrio e DRE por horizonte.

## Premissas iniciais da versão

- Pedidos/dia: M1 90; M6 120; estabilizado 170.
- Fundo cooperado de marketing 1%; marketing local 1%; pagamentos e delivery 3%.
- Equipe 5; pró-labore mensal R$ 5.000.
- Parcela do financiamento R$ 9.000 por 48 meses.
- Condomínio/fundo/IPTU R$ 500; utilidades/manutenção/administração R$ 5.000; seguro/sistema/outros R$ 300.
- Reajuste anual dos custos fixos 3,5%.

## Atualizar o repositório GitHub

Copie esta versão para o `index.html` do clone local do repositório e envie a alteração:

```bash
cp "/home/haroldo/Documents/Codex/2026-10-25/aces/outputs/simuladorboali/index.html"    "/home/haroldo/Documentos/ChatGPT/simuladorboali-easypanel/simuladorboali/index.html"
cd "/home/haroldo/Documentos/ChatGPT/simuladorboali-easypanel/simuladorboali"
git add index.html
git commit -m "Atualiza premissas e cálculos do simulador Boali"
git push origin main
```

## Deploy no EasyPanel

1. Abra o serviço App do simulador, ligado ao repositório `automacaopaivaimobiliaria26/simulador_boali`, branch `main`, Build Path `/` e Dockerfile `Dockerfile`.
2. Mantenha em **Domains**: Host `www.paivanegociosimobiliarios.com.br`, Path `/simuladorboali`, HTTPS ativado, protocolo HTTP e porta `8080`.
3. Clique em **Deploy** (a menos que Auto Deploy esteja ativo).
4. Confira `https://www.paivanegociosimobiliarios.com.br/simuladorboali` em celular e desktop.

## Observação sobre premissas salvas

As alterações já salvas no `localStorage` do mesmo navegador prevalecem sobre os novos valores iniciais. Para iniciar com as premissas v8 nesse navegador, use **Restaurar cenário inicial** uma vez. O armazenamento é local ao navegador e não é compartilhado entre visitantes ou dispositivos.

O modelo subtrai as parcelas mensais de financiamento pelo prazo informado, mas não recebe um valor de principal financiado. Portanto, o desembolso inicial considera CAPEX e capital de giro integralmente pagos no início; informe isso ao interpretar VPL, TIR e payback.
