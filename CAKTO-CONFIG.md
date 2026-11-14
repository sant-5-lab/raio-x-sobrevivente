# Cakto · configuração do funil Bunker Urbano 72H (14/11/2026)

Base: `../estrategia-funil-protocolo-blecaute-72h.md` (seção v2) + `COPY-QUIZ.md`. PDFs em `../ebooks/pdf/`.

## Escada de ofertas

| Papel | Produto | PDF | Preço |
|---|---|---|---|
| **Principal** (já criado na Cakto, id `54855669-b2de-4826-971b-6d6040a28d75`) | Guia Bunker Urbano 72H | `01-guia-bunker-urbano-72h.pdf` | R$ 19,90 até 17/11 23h59 → **R$ 27** em 18/11 |
| Order bump 1 | Arsenal do Sobrevivente | `02-arsenal-do-sobrevivente.pdf` | + R$ 9,90 |
| Order bump 2 | Despensa Bunker | `03-despensa-bunker.pdf` | + R$ 12,90 |
| Upsell 1 clique | Bunker 7 Dias | `04-bunker-7-dias.pdf` | R$ 47 |
| Downsell (só pra quem recusou o upsell) | Energia 7 Dias | `05-energia-7-dias.pdf` | R$ 19,90 |

Meta: ticket médio ≈ R$ 31,90 (bump 1 em 30%, bump 2 em 20%, upsell 10%, downsell 10% de quem recusou).

## Textos

**Descrições dos produtos**
- Arsenal: "Os equipamentos que funcionam quando tudo falha, por faixa de preço, e os que parecem bons mas falham. Acesso imediato por e-mail."
- Despensa: "3 dias de comida sem geladeira e sem tomada: cardápio + lista de mercado para 2, 4 e 6 pessoas."
- Bunker 7 Dias: "72 horas é o mínimo. Água, comida, energia, saneamento, segurança e comunicação para 7 dias, com mais projetos DIY."
- Energia 7 Dias: "Manter celular, luz e internet por uma semana: power bank, painel solar e power station, com o que vale e o que não vale a compra."

**Order bump 1 (Arsenal)** — título: "Arsenal do Sobrevivente". Chamada: "✅ Sim! Quero saber quais lanternas, power banks e rádios funcionam de verdade quando tudo apaga, e quais quebram na primeira noite."
**Order bump 2 (Despensa)** — título: "Despensa Bunker". Chamada: "✅ Sim! Quero o cardápio de 3 dias sem geladeira e sem tomada, com a lista de mercado pronta para o tamanho da minha família."

**Upsell** — título: "Espera. 72 horas é o mínimo. E se a luz demorar uma semana para voltar?" Aceitar: "Sim, quero o Bunker 7 Dias" · Recusar: "Não, 72 horas me bastam".
**Downsell** — título: "Tudo bem. Leve só o que mantém a casa ligada por 7 dias." Aceitar: "Quero a Energia 7 Dias".

## Regras
- Garantia 7 dias (CDC art. 49).
- Nada de "vai ter apagão dia 17" nem "oficial da Defesa Civil" (CDC art. 37 §2º).
- Virada de preço do principal em 18/11 **tem que ser feita na Cakto** (a página muda sozinha; o checkout não).
- Página de obrigado do principal → `https://sant-5-lab.github.io/raio-x-sobrevivente/quiz.html#obrigado` (entrega o Plano Bunker personalizado).

## Depois de criar
1. Colar o link do checkout em `quiz.html` → `CONFIG.checkout` (linha ~245) e confirmar os nomes dos campos de pré-preenchimento em `CONFIG.prefill` (hoje `name`, `email`, `phone`).
2. Trocar `#AFILIADO-*` e `#LINK-PLANO` nos ebooks (ver HISTORICO 11/11) e reexportar com `ebooks/exportar-pdfs.bat`.
3. Teste de compra ponta a ponta (principal + 2 bumps → upsell → downsell → obrigado).
