# Livro de Receitas

Aplicação web de receitas feita em **React + TypeScript** para a disciplina de Front-end Frameworks (Ciência da Computação, AV2).
Os dados vêm da API pública [TheMealDB](https://www.themealdb.com) (sem chave). As receitas favoritas ficam salvas no `localStorage`.

## Como rodar

Pré-requisito: Node.js 18 ou superior.

```bash
npm install
npm run dev      # abre em http://localhost:5173
npm run build    # gera a versão de produção em /dist
```

## Páginas (rotas)

| Rota | Página |
|---|---|
| `/` | Início, com receita sugerida (aleatória) |
| `/receitas` | Lista com busca e filtro por categoria |
| `/receitas/:id` | Detalhe da receita |
| `/favoritos` | Receitas favoritadas |
| `/sobre` | Sobre o projeto |
| `/contato` | Formulário de contato |

## Hooks utilizados

| Hook | Onde |
|---|---|
| `useState` | `Receitas`, `FormularioContato`, `useFetch` |
| `useEffect` | `useFetch`, `useDebounce`, `BarraBusca` |
| `useContext` | `FavoritosContext` (hook `useFavoritos`) |
| `useRef` | `BarraBusca` (foco automático no campo) |
| `useMemo` | `Receitas` (filtro da lista), `FavoritosContext` |
| Custom hooks | `useFetch`, `useDebounce`, `useLocalStorage`, `useFavoritos` |

## Integrantes e componentes

Cada integrante é responsável pela criação e explicação dos 2 componentes abaixo.

| Integrante | Componentes | Arquivos |
|---|---|---|
| Jackson Emanuel | `Navbar`, `Footer` | `src/components/Navbar.tsx`, `Footer.tsx` |
| Weslley Natanael | `CardReceita`, `ListaReceitas` | `src/components/CardReceita.tsx`, `ListaReceitas.tsx` |
| Ana Jéssica | `BarraBusca`, `FiltroCategoria` | `src/components/BarraBusca.tsx`, `FiltroCategoria.tsx` |
| Miguel Neto | `BotaoFavorito`, `FormularioContato` | `src/components/BotaoFavorito.tsx`, `FormularioContato.tsx` |
| Diego Guimarães | `Loading`, `MensagemErro` | `src/components/Loading.tsx`, `MensagemErro.tsx` |

## Estrutura

```
src/
├── components/   # 10 componentes reutilizáveis
├── pages/        # 6 páginas + 404
├── context/      # FavoritosContext (Context API)
├── hooks/        # useFetch, useDebounce, useLocalStorage
├── services/     # api.ts (chamadas à TheMealDB)
└── types.ts      # interfaces TypeScript
```

## Telas

> Adicionem aqui os prints (pasta `prints/`): Início, Receitas, Detalhe, Favoritos, Contato.
