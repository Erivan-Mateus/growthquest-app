# GrowthQuest

App de hábitos em formato RPG, feito em React + Vite. Progresso salvo no `localStorage` do navegador.

## Rodar localmente

```bash
npm install
npm run dev
```

Abre em `http://localhost:5173`.

## Deploy no Vercel

### Opção A — pelo site do Vercel (mais fácil)

1. Suba esta pasta para um repositório no GitHub (crie um repo novo, faça `git init`, `git add .`, `git commit -m "primeiro commit"`, `git push`).
2. Entre em [vercel.com](https://vercel.com), clique em **Add New → Project**.
3. Selecione o repositório. O Vercel detecta automaticamente que é um projeto **Vite** — não precisa mudar nada nas configurações de build.
4. Clique em **Deploy**.

### Opção B — pela linha de comando (sem precisar de GitHub)

```bash
npm install -g vercel
cd growthquest-app
vercel
```

Siga as perguntas no terminal (login, nome do projeto, etc). Ao final ele te dá uma URL pública.

## Estrutura

- `src/App.jsx` — o app inteiro (componente `GrowthQuestApp`)
- `src/main.jsx` — ponto de entrada que monta o React na página
- `index.html` — HTML base que o Vite usa
- `package.json` — dependências: `react`, `react-dom`, `lucide-react`, `recharts`

## Observação sobre o save

Os dados ficam em `localStorage`, presos ao navegador/dispositivo onde você usa o site. Limpar o cache do navegador apaga o progresso. Se um dia você quiser sincronizar entre aparelhos, vai precisar trocar essa parte por um banco de dados (ex: Supabase, Firebase, Vercel KV) — pode pedir ajuda pra isso quando quiser.
