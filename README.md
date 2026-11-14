# Match Ghost - Alecrim Digital 🌿

Uma aplicação web inteligente (SaaS B2C) desenvolvida para otimizar perfis profissionais e currículos, garantindo que eles superem os filtros dos sistemas ATS (Applicant Tracking Systems). 

🔗 **Link da Aplicação Publicada:** [https://alecrim-digital-match-dio.lovable.app](https://alecrim-digital-match-dio.lovable.app)

---

## 🎯 1. O Problema que Resolvemos
Muitos profissionais altamente qualificados são descartados logo na primeira etapa de processos seletivos não por falta de capacidade, mas porque seus currículos não "falam a mesma língua" dos robôs de triagem (ATS). Adaptar o currículo manualmente para cada vaga exige muito tempo e esforço. O **Match Ghost** automatiza essa tradução, destacando os pontos fortes do candidato sem perder a ética profissional.

---

## ⚙️ 2. Como a Análise Funciona (O Fluxo)

A plataforma foi desenhada para ter o menor atrito possível para o usuário:

1. **Lead Capture (Login sem senha):** O usuário insere apenas o e-mail para acessar a plataforma. Isso reduz a fricção e permite a captação do lead.
2. **Entrada de Dados (Copiar e Colar):** O usuário cola o texto bruto do seu currículo/LinkedIn na primeira caixa, e a descrição da vaga desejada na segunda.
3. **Processamento da IA:** A aplicação envia os dados para a Inteligência Artificial, que cruza os requisitos da vaga com o histórico do candidato.
4. **O Resultado (Dashboard):**
   - Exibe o **Percentual de Match** geral.
   - Lista as **Palavras-chave** (encontradas e faltantes).
   - Gera uma **Nova Bio ATS-Friendly** ajustada e pronta para exportação.
   
⚠️ **Regra de Ouro da Aplicação:** A IA possui instruções sistêmicas estritas (visíveis no disclaimer da interface) de que ela deve **apenas realçar e reescrever** com as palavras-chave corretas. **A IA nunca inventa ou alucina experiências que o candidato não possui.**

---

## 🤖 3. O Mega Prompt Original

A primeira versão da aplicação foi construída utilizando a IA do Lovable (Claude 3.5 Sonnet) com o seguinte mega prompt estrutural, já contemplando o Design System da marca *alecrim.digital*:

> "Act as an expert Frontend Developer and UX/UI Designer. Build a complete React MVP called 'Match Ghost' using Tailwind CSS, shadcn/ui, and Lucide React icons.
> 
> **Design System:** Strictly use these colors: Primary `#123D32`, Secondary `#1B493D`, Accent `#B99A64`, Background `#FAF7F0`, Surface `#F4EBDD`, Text `#263A35`. Typography: 'Cormorant Garamond' for headings, 'Montserrat' for body text.
> 
> **State 1 (Auth):** A clean card with an email input and password to sign up/login using Supabase Auth.
> 
> **State 2 (Input):** Two large textareas side-by-side. Left: 'Cole seu currículo'. Right: 'Cole a vaga'. A large button: 'Analisar Match com IA'. Add a visible disclaimer: 'A IA apenas otimiza o texto para ATS, nunca inventamos experiências que você não tem'.
> 
> **State 3 (Results):** When analyzed, show a loading spinner, then use Gemini AI to generate: 1) Match percentage. 2) List of keywords found and missing. 3) A rewritten ATS-friendly text ready to copy.
> Make the UI premium, minimalist, and responsive."

---

## 🛠️ 4. Evolução e Ajustes Pós-Geração

A primeira geração entregou a estrutura perfeitamente, mas exigiu duas rodadas principais de refinamento focadas em UX e Branding:

* **Ajuste 1: Remoção de Senhas (Foco em Conversão).** 
  * *O que mudei:* Solicitei à IA que removesse o fluxo de criação de conta com senha e e-mail de confirmação. 
  * *Por quê:* Para um MVP de validação, qualquer campo extra reduz a adoção. O sistema foi ajustado para salvar o e-mail em um banco de dados no *Lovable Cloud* (Lead Capture) e liberar o acesso imediatamente.
* **Ajuste 2: Correção do Design System (Alucinação Visual).**
  * *O que mudei:* A IA inicialmente adicionou texturas botânicas em 3D/realistas ao fundo. Fiz o upload da minha logo oficial no chat e enviei um prompt secundário proibindo folhagens realistas e forçando o uso de estilo *line-art minimalista* (ícone flat ao lado do texto).
  * *Por quê:* Para manter a sofisticação da identidade visual da Alecrim Digital.
* **Ajuste 3: Refinamento do Prompt Interno da IA.**
  * *O que mudei:* Garanti que as instruções de background do modelo gerassem o novo texto sem adicionar jargões artificiais, mantendo a autenticidade do candidato.

---

## 📸 5. Demonstração de Uso

*(Adicione aqui 3 prints da sua tela: 1. Tela de Login inicial; 2. Telas das duas caixas de texto preenchidas; 3. Tela de resultado com o gráfico e o texto otimizado)*

<img width="1355" height="617" alt="image" src="https://github.com/user-attachments/assets/87475206-a57c-4f6b-bd3c-9cc7638e4f4e" />
<img width="1322" height="603" alt="image" src="https://github.com/user-attachments/assets/c6674ff8-1227-436f-a255-24c739918d09" />
<img width="1330" height="586" alt="image" src="https://github.com/user-attachments/assets/5271c5df-5924-440d-8494-6794e4ad953d" />

---

## 💻 6. Tecnologias Utilizadas
* **Frontend:** React, Tailwind CSS, Vite.
* **Componentes & UI:** shadcn/ui e Lucide React.
* **Backend & Auth:** Lovable Cloud.
* **Inteligência Artificial:** Integração via prompts de sistema estruturados para análise de linguagem natural (LLM).

---
*Desenvolvido por [Daniela Alecrim/Alecrim Digital] para validação de produto e conclusão de desafio técnico.*
