<div align="center">

# ⛏ StackVault

### Cada stack conta.

Rastreador de coleção de itens do **Minecraft Survival (Java & Bedrock 26.3)** — pesquise, filtre, marque e sincronize todo o seu progresso direto no navegador.

[![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)](https://developer.mozilla.org/docs/Web/HTML)
[![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)](https://developer.mozilla.org/docs/Web/CSS)
[![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)](https://developer.mozilla.org/docs/Web/JavaScript)
[![Supabase](https://img.shields.io/badge/Supabase-3ECF8E?style=for-the-badge&logo=supabase&logoColor=white)](https://supabase.com)
[![GitHub Pages](https://img.shields.io/badge/GitHub%20Pages-222222?style=for-the-badge&logo=githubpages&logoColor=white)](https://brieeldev.github.io/minecraft/)

### 🔗 [**Abrir o site**](https://brieeldev.github.io/stack_vault/)

</div>

---

## 📖 Sobre

O **StackVault** é um checklist interativo para quem quer completar **100% da coleção de itens** do Minecraft Survival. São **1.532 itens** organizados em **38 categorias**, com ícones oficiais em alta resolução.

O progresso é salvo **localmente no navegador** e, opcionalmente, **na nuvem** para ser compartilhado com amigos em uma mesma coleção.

> 💡 Funciona offline para marcar itens; a nuvem é usada apenas para sincronizar e compartilhar.

---

## ✨ Funcionalidades

- 🎯 **Checklist completo** — marque/desmarque cada item coletado.
- 🔍 **Busca e filtros** — pesquise por nome (em qualquer idioma), filtre por categoria e status (faltantes / coletados).
- 🗂️ **38 categorias** — Minérios, Ferramentas, Armas, Armaduras, Redstone, Nether, End, Comidas e muito mais.
- 🖼️ **Ícones oficiais** — carregados da API `mc-api.bisai.dev`, com normalização de textura (corrige tiras animadas e imagens não quadradas).
- 🌍 **10 idiomas** — toda a interface e os nomes dos itens são traduzidos.
- 🏅 **Títulos/ranks** — Novato → Explorador → Minerador → Colecionador → Sobrevivente → Lenda do Overworld.
- 📊 **Painel de progresso** — porcentagem geral e progresso por categoria.
- ☁️ **Coleções compartilhadas** — login por e-mail/senha (Supabase), crie uma coleção ou entre pelo código e sincronize com os amigos.
- 👥 **Gestão de membros** — veja quem entrou/saiu (com data e hora) e remova membros (só o dono).
- 💾 **Backup/importação** — exporte e restaure seu progresso em JSON.
- 📱 **Responsivo** — menu inferior e dropdowns que abrem sempre para baixo.

---

## 🌍 Idiomas

`pt` · `en` · `es` · `fr` · `de` · `it` · `ja` · `ko` · `zh` · `ru`

A tradução cobre **textos da interface, nomes das categorias, ranks e nomes oficiais dos itens**.
O nome **StackVault** permanece igual (ou transliterado) em todos os idiomas.

---

## 🧱 Tecnologias

| Camada | Uso |
| --- | --- |
| **HTML/CSS/JS puro** | Aplicação em um único arquivo `index.html`, sem build |
| **Bootstrap 5.3** | Base de estilos |
| **Supabase** | Autenticação e banco (coleções, membros e histórico) |
| **mc-api.bisai.dev** | Texturas dos itens |
| **PrismarineJS minecraft-assets** | Fallback de dados de assets |
| **GitHub Pages** | Hospedagem estática |

---

## 🚀 Como usar

### Localmente

Basta abrir o `index.html` no navegador — não há dependências para instalar.

```bash
# opcional: servir localmente
python -m http.server 8000
# depois acesse http://localhost:8000
```

### Nuvem (coleções compartilhadas)

1. Crie um projeto no [Supabase](https://supabase.com).
2. Execute o `supabase_schema.sql` no SQL Editor (estrutura principal).
3. Execute o `supabase_migration_member_events.sql` (histórico de entrada/saída de membros).
4. Ajuste a URL e a chave anônima do Supabase no topo do script do `index.html`.

**Tabelas principais**

| Tabela | Descrição |
| --- | --- |
| `collections` | Coleções criadas (nome, código de convite, dono) |
| `collection_members` | Quem participa de cada coleção |
| `collection_member_events` | Histórico de entrada/saída de membros |
| `progress` | Itens marcados por usuário/coleção |

---

## 📁 Estrutura

```
.
├── index.html                          # Aplicação completa (SPA de arquivo único)
├── supabase_schema.sql                 # Schema principal do banco
├── supabase_migration_member_events.sql# Migração do histórico de membros
├── progresso_minecraft_26_3.json       # Exemplo de progresso exportado
└── backup_minecraft_26_3_...json       # Exemplo de backup
```

---

## 🗺️ Roadmap

- [ ] Mais idiomas
- [ ] Modo escuro/claro
- [ ] Estatísticas avançadas por categoria
- [ ] Exportar coleção como imagem

---

<div align="center">

Feito para jogadores de Minecraft ⛏

</div>
