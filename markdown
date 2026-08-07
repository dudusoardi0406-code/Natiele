# Blueprint — Página de Bio de Alta Conversão
> Estrutura destilada da bio da Bárbara Torres (Método Comunicando),
> com as correções aplicadas.

---

## 1. Sistema visual (defina ANTES de montar a página)

| Elemento | Decisão | Exemplo de referência |
|---|---|---|
| Fundo | 1 cor escura e "suja", nunca preto puro | `#1E1916` marrom-café |
| Acento | 1 cor quente para CTA e pontuação | vermelho tijolo / coral |
| Tipo display | Serifada com personalidade, só em títulos | Moneta Sans, Playfair, Canela |
| Tipo texto | Sans neutra, 2 pesos no máximo | Manrope, Inter |
| Motivo gráfico | 1 elemento repetido em TODOS os cards | ingresso + código de barras |
| Imagética | 1 universo visual coerente | pintura clássica com filtro quente |

**Regra de ouro:** um único motivo gráfico repetido cria mais marca
que cinco efeitos diferentes.

---

## 2. Estrutura da página (ordem importa)

### Bloco 1 — Identidade (acima da dobra)
- [ ] Foto de rosto redonda, olhando pra câmera
- [ ] Nome em tipo display
- [ ] **Uma frase de promessa**, não uma bio.
      Fórmula: `[verbo de aprendizado] + [habilidade] + [resultado tangível]`
      > "Aprenda a se comunicar com clareza e conquiste respeito, audiência e autoridade."
- [ ] Ícones sociais em linha (resolve quem só quer seguir)
- [ ] Assinatura/tagline discreta no fundo

### Bloco 2 — Oferta principal (1 card, destacado)
Card visualmente diferente dos outros: borda, brilho ou cor exclusiva.
Este é o único CTA que você realmente quer que cliquem.

### Bloco 3 — Ofertas secundárias
Produto pago → produto de entrada → conteúdo gratuito.
**Dinheiro antes de conteúdo grátis.**

### Bloco 4 — Prova social  ⬅️ FALTA no original
- [ ] Número de audiência ("+180 mil alunos" / "2M de visualizações")
- [ ] 1 depoimento curto com foto e nome
- [ ] Logos de veículos ou marcas atendidas

### Bloco 5 — Captura de lead  ⬅️ FALTA no original
- [ ] Campo de e-mail OU botão de grupo/lista de WhatsApp
- [ ] Isca clara: "Receba 1 técnica de comunicação por semana"

### Bloco 6 — Contato e rodapé
- [ ] Seção separada por título + linha divisória
- [ ] E-mail visível em texto (não só ícone)
- [ ] `© Ano — Nome`

---

## 3. Anatomia de um card

Cada card precisa de 4 camadas:

1. **Categoria** em display grande — `MENTORIA`, `YOUTUBE`
2. **Subtítulo/nome próprio** — `Vértice`
3. **Benefício em 1–2 linhas**, com a parte decisiva em cor de acento
   > "Construa autoridade com autenticidade e um negócio digital sólido,
   >  *sem fórmulas genéricas.*"
4. **Ornamento da marca** — código de barras, numeração, linha curva

❌ Errado: `Meu curso`
✅ Certo: `MEUS CURSOS — Acelere seu crescimento com sua voz e seus conteúdos`

---

## 4. Checklist técnico (o que o original erra)

- [ ] **Texto em HTML, não dentro da imagem.**
      Use a arte só como fundo (`background-image`) e o texto por cima em CSS.
      Ganha SEO, acessibilidade, responsividade e velocidade.
- [ ] `alt` descritivo em toda imagem
- [ ] WebP/AVIF + `loading="lazy"` nos cards abaixo da dobra
- [ ] Revisar as artes: **nenhum lorem ipsum publicado**
- [ ] Um mesmo destino = uma mesma URL (ícone e card não podem divergir)
- [ ] UTM colada corretamente (`&utm_source=` se a URL já tem `?`)
- [ ] E-mail sempre via `mailto:`, nunca via link do Gmail
- [ ] Estado de `:hover` e `:focus` visível em todo card
- [ ] Área de toque mínima de 44×44px nos ícones
- [ ] Testar primeiro em 390px de largura — bio é mobile-first
- [ ] Pixel/GA4 + evento de clique por card

---

## 5. Nomenclatura de UTM

Sem padrão, o relatório vira lixo em duas semanas: `Instagram`, `instagram`
e `IG` viram três linhas diferentes do mesmo tráfego.

### Os 4 parâmetros e o que cada um responde

| Parâmetro | Pergunta que responde | Valor na bio |
|---|---|---|
| `utm_source` | De qual rede veio? | `instagram`, `tiktok`, `youtube`, `linkedin` |
| `utm_medium` | De qual tipo de link? | **sempre** `bio` (separa de `ads`, `email`, `stories`) |
| `utm_campaign` | Qual card foi clicado? | `mentoria-vertice`, `curso-comunicando`, `ebook-voz` |
| `utm_content` | Qual variação/posição? | `card-1`, `card-3`, `botao-topo` |

`utm_term` não se usa aqui — é de busca paga.

### Regras de escrita (inegociáveis)

- Tudo em **minúsculas** — UTM diferencia maiúscula de minúscula
- **Sem acento e sem cedilha** — `mentoria` e não `mentoría`
- **Hífen** como separador, nunca espaço nem underline
- Nome do card ≠ nome da campanha de vendas: aqui é o **destino**, não a promoção
- **Depois de publicado, não se renomeia.** Renomear quebra a série histórica

### Montagem

```
https://destino.com.br/pagina?utm_source=instagram&utm_medium=bio&utm_campaign=mentoria-vertice&utm_content=card-1
```

O primeiro parâmetro entra com `?`, os demais com `&`.
Se a URL **já tem** `?` (ex.: `?ref=abc`), o primeiro UTM também entra com `&`:

```
❌ https://destino.com.br/p?ref=abc?utm_source=instagram
✅ https://destino.com.br/p?ref=abc&utm_source=instagram
```

### Tabela de controle (mantenha uma, versionada)

| Card | Destino | source | medium | campaign | content |
|---|---|---|---|---|---|
| Mentoria Vértice | hotmart | `instagram` | `bio` | `mentoria-vertice` | `card-1` |
| Curso Comunicando | hotmart | `instagram` | `bio` | `curso-comunicando` | `card-2` |
| Canal YouTube | youtube | `instagram` | `bio` | `youtube-canal` | `card-3` |
| Lista WhatsApp | grupo wa | `instagram` | `bio` | `lista-whatsapp` | `captura` |

Uma linha por card, preenchida **antes** de publicar. É essa tabela que
permite trocar um card de posição e ainda saber o que mudou.

Sem `utm_content` você não descobre qual card converte.

---

## 6. Perguntas antes de publicar

1. Em 3 segundos dá pra saber **o que a pessoa ensina** e **pra quem**?
2. Qual é o **único** link que eu quero que cliquem? Ele está destacado?
3. Existe algum motivo pra confiar nessa pessoa nesta página?
4. Se o Instagram cair amanhã, eu tenho como falar com essa audiência?
5. Cada card promete um **benefício** ou só nomeia um **destino**?
