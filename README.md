# Simulação de Phishing Financeiro — Mercado Pago

> Página de demonstração educacional que replica as técnicas visuais e comportamentais utilizadas em ataques de phishing financeiro, com aparência do Mercado Pago.

![Finalidade](https://img.shields.io/badge/finalidade-educacional-orange.svg)
![Tecnologia](https://img.shields.io/badge/tech-HTML%20%2F%20CSS%20%2F%20JS-blue.svg)
![Dependências](https://img.shields.io/badge/depend%C3%AAncias-nenhuma-green.svg)

> **Aviso:** Este material é estritamente para fins de conscientização em segurança digital, treinamento de equipes e pesquisa. Nunca utilize para enganar pessoas reais ou coletar dados sem consentimento.

---

## Objetivo

Demonstrar na prática como ataques de phishing financeiro funcionam, incluindo:

- Clonagem visual fiel de marcas conhecidas (Mercado Pago / Visa)
- Coleta de dados pessoais sensíveis em formulários convincentes
- Simulação de análise de crédito para gerar senso de urgência e legitimidade
- Cobrança fraudulenta de "taxa de envio" via PIX após falsa aprovação

---

## Fluxo do ataque simulado

```
Vítima acessa o link
        ↓
Landing page clonada do Mercado Pago
        ↓
Formulário coleta: nome, CPF, data de nascimento,
e-mail, celular, CEP, endereço e renda mensal
        ↓
Contagem regressiva fake ("Analisando seu pedido...")
        ↓
Modal de "aprovação" com limite de R$ 7.000
        ↓
Cobrança de R$ 29,90 via PIX ("taxa de envio do cartão")
        ↓
QR Code e código PIX exibidos com timer de 15 minutos
```

---

## Técnicas de engenharia social simuladas

| Técnica | Implementação na página |
|---------|------------------------|
| Identidade visual clonada | Logo, paleta de cores e tipografia do Mercado Pago |
| Prova social | "+50 mi clientes", badges de segurança, selos Visa Gold |
| Urgência | Timer de 15 min no PIX, animação de "análise em tempo real" |
| Legitimidade técnica | Chip EMV, animação 3D do cartão, QR Code realista |
| Aprovação garantida | 100% de aprovação independente dos dados digitados |
| Ancoragem de valor | Exibe limite de R$ 7.000 antes de pedir R$ 29,90 |
| Campo sensível | CPF, data de nascimento, celular e endereço completo |

---

## Estrutura da página

| Seção | Descrição |
|-------|-----------|
| Header sticky | Logo falso + nav + CTA "Peça seu cartão" |
| Hero | Cartão 3D animado + estatísticas de confiança fabricadas |
| Benefícios | Grid com 6 cards replicando benefícios reais do produto |
| Como funciona | 3 passos para minimizar fricção e transmitir simplicidade |
| Formulário | Coleta de dados em 4 etapas com máscaras de CPF, celular e CEP |
| Modal de aprovação | Countdown + confetti + limite animado de R$ 7.000 |
| Tela PIX | QR fake + código copia-e-cola + timer regressivo |
| FAQ | Respostas que aumentam credibilidade e reduzem dúvidas |
| Footer | Textos legais copiados da página real |

---

## Dados coletados pelo formulário

- Nome completo
- CPF (com máscara automática)
- Data de nascimento
- E-mail
- Celular
- CEP, endereço, cidade e estado
- Faixa de renda mensal

---

## Tecnologia

Arquivo único, sem dependências externas além de Google Fonts:

- **HTML5** semântico
- **CSS3** — variáveis, grid, animações, `@keyframes`, responsivo completo
- **JavaScript** vanilla — máscaras de input, modal, countdown, confetti, timer PIX, clipboard API

---

## Como usar (ambiente controlado)

```bash
# Basta abrir o arquivo no navegador
open cartao-mercadopago-v2.html
```

Não requer servidor, build ou instalação.

---

## Sinais de alerta que a página simula esconder

Para fins didáticos, estes são os sinais que uma vítima real deveria observar:

- URL não é `mercadopago.com.br`
- Nenhuma validação real dos dados inseridos
- Aprovação de crédito instantânea e universal (irreal)
- "Taxa de envio" cobrada antes de qualquer entrega — prática inexistente no Mercado Pago legítimo
- QR Code não é funcional e o código PIX é estático/fixo
- Dados do formulário não são enviados a nenhum servidor seguro

---

## Aviso legal

Este repositório é destinado exclusivamente a:

- Treinamentos de conscientização em segurança da informação
- Simulações de phishing autorizadas (pentest social)
- Pesquisa acadêmica e educação em cibersegurança

O uso para fraude, captação indevida de dados ou qualquer atividade ilegal é expressamente proibido e sujeito às penalidades da **Lei nº 12.737/2012 (Lei Carolina Dieckmann)**, **LGPD** e demais legislações aplicáveis.

---

## Licença

MIT — para uso educacional.
