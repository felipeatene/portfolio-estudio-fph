# Estúdio FPH — Portfolio Website

Site portfolio profissional desenvolvido para o Estúdio FPH, com foco em arquitetura contemporânea, BIM, sofisticação visual e captação de clientes.

## Objetivo

Criar uma presença digital premium que transmita autoridade técnica, estética refinada e confiança.

## Estrutura do Projeto

### 1. Arquivos Principais

```
portfolio-estudio-fph/
├── index.html              # Arquivo HTML principal (single-page)
├── styles.css              # Estilos CSS (responsivo, mobile-first)
├── README.md               # Documentação do projeto
├── .nojekyll               # Flag para GitHub Pages
├── arquivos/               # Pasta com ativos (imagens, logos, PDFs)
├── .github/                # Configurações GitHub
└── .git/                   # Versionamento Git
```

### 2. Ativos (Pasta `arquivos/`)

**Logos & Branding:**
- `logo-fph.svg` — Logo do Estúdio FPH (SVG vetorizado)

**Imagens:**
- `hero-brasil.jpg` — Background/herói da seção inicial
- `foto_perfil.jpg` — Foto de perfil de Felipe Guimarães
- `cover-hospital.jpg` — Capa visual: Projeto Hospital Sol
- `cover-ferrosos.jpg` — Capa visual: Projeto Ferrosos Baratinha
- `cover-femsa.jpg` — Capa visual: Projeto FEMSA Coca-Cola

**Documentos (PDFs de Projetos):**
- Hospital Sol:
  - `006-2024-01-EX-ARQ-GER-DES-002_R00.pdf` (Implantação)
  - `006-2024-01-EX-ARQ-GER-DES-005_R00.pdf` (Drywall)
- Ferrosos Baratinha:
  - `0623FB-00-15-9067.pdf` (Cozinha)
  - `0623FB-00-15-9071.pdf` (Detalhamentos)
- FEMSA Coca-Cola:
  - `FEMSA Coca Cola - Itabirito.pdf` (Planta de Cotas e Cortes)

### 3. Seções & Componentes HTML

#### **Header (Navegação Fixa)**
- Logo clicável (link para #top)
- Menu primário: Projetos | Serviços | Estúdio | Contato
- Botão de ação (WhatsApp)
- Classes CSS: `.site-header`, `.primary-nav`, `.brand`

#### **Hero Section**
- Background com imagem herói
- Tagline: "Arquitetura · BIM · Documentação Técnica"
- H1 com ênfase (*silenciosa*)
- Subtítulo (hero-lead)
- 2 CTAs: "Ver projetos" e "Falar com o estúdio"
- Metadados: Localização (BH · Brasil) + período (2020 — 2026)
- Classes CSS: `.hero`, `.hero-inner`, `.hero-media`, `.hero-actions`

#### **Seção Projetos** (`#projetos`)
- Grid de 3 projetos em destaque
- Cada projeto contém:
  - Imagem de capa clicável
  - Badge de categoria
  - Título + Ano
  - Descrição breve
  - **Modal Interativo:**
    - 6 Accordions (Resumo, Escopo, Desafios, Indicadores, Tecnologias, Resultados)
    - Visualizador PDF em iframe
    - Abas para trocar entre múltiplos PDFs
    - Botão de fechar (✕)
- Projetos: Hospital Sol | Ferrosos Baratinha | FEMSA Coca-Cola
- Classes CSS: `.project`, `.project-list`, `.modal-backdrop`, `.accordion`

#### **Seção Serviços** (`#servicos`)
- Grid de 6 serviços em layout responsivo
- Cada serviço com:
  - Ícone SVG customizado (coluna, cubo, câmera, documento, apresentação, caneta)
  - Título (h4)
  - Descrição breve
- Serviços oferecidos:
  1. Projetos Arquitetônicos (residencial, comercial, industrial, hospitalar)
  2. Modelagem e Gestão BIM (Revit, Archicad, IFC)
  3. Renderização 3D (3DS Max, Lumion, Unreal Engine)
  4. Documentação Técnica (pranchas, detalhamentos, aprovação)
  5. Consultoria e Treinamento (suporte BIM, memoriais)
  6. Design Gráfico (identidade visual, diagramação)
- Classes CSS: `.services-grid`, `.service`, `.service-icon`

#### **Seção Sobre** (`#sobre`)
- Layout 2 colunas (grid):
  - **Coluna 1:** Foto + Caption "Felipe Guimarães · Fundador · Arquiteto & BIM Manager"
  - **Coluna 2:** Conteúdo textual
- Conteúdo:
  - Tagline: "Estúdio"
  - H2: "Sobre o Estúdio"
  - Parágrafos descritivos (missão, clientes, formação)
  - Lista de 6 competências principais
  - Link para LinkedIn
- Classes CSS: `.about-grid`, `.about-photo`, `.about-text`, `.competencias`

#### **Seção Contato** (`#contato`)
- Layout 2 colunas:
  - **Coluna 1:** Informações de contato
    - Texto principal
    - Localização: "Belo Horizonte · Minas Gerais · Brasil"
    - 3 botões de contato (WhatsApp, E-mail, LinkedIn)
  - **Coluna 2:** Formulário interativo
    - Título: "Envie uma mensagem"
    - Campo: Nome
      - `type="text"` 
      - `id="contato-nome"` 
      - `name="nome"` 
      - `autocomplete="name"` ✅
    - Campo: E-mail
      - `type="email"` 
      - `id="contato-email"` 
      - `name="email"` 
      - `autocomplete="email"` ✅
    - Campo: Mensagem
      - `type="textarea"` 
      - `id="contato-mensagem"` 
      - `name="mensagem"` 
      - `autocomplete="off"` ✅
    - Botão: Submit "Enviar mensagem"
- Classes CSS: `.section-contact`, `.contato-grid`, `.contato-form`, `.contact-btn`
- Validação HTML5 (required attributes)

#### **Footer**
- 2 linhas de conteúdo:
  - **Linha 1:** Logo + Descrição breve
  - **Linha 2:** Links de navegação + Links sociais + Copyright
- Seções:
  - Navegar: Projetos, Serviços, Estúdio, Contato
  - Social: LinkedIn, WhatsApp, E-mail
  - Copyright © 2026 + "Voltar ao topo ↑"
- Classes CSS: `.site-footer`, `.footer-grid`, `.footer-cols`

### 4. Tecnologias & Dependências

**Frontend:**
- HTML5 (semântico, acessível, ARIA labels)
- CSS3 (Grid, Flexbox, media queries, responsivo)
- JavaScript vanilla (dom manipulation, modais, accordions)
- SVG (ícones inline, logo vetorizado)

**Tipografia (Google Fonts CDN):**
- `Cormorant Garamond` (400, 500, 600) — Títulos e elementos premium
- `Inter` (300, 400, 500, 600) — Body text e componentes UI

**Recursos Externos:**
- **Integração WhatsApp:** Links wa.me/ (sem backend)
- **Integração LinkedIn:** Links linkedin.com
- **Integração E-mail:** Links mailto:
- **PDFs:** Embutidos em iframes (visualizador nativo do navegador)

**Hospedagem:**
- GitHub Pages (build automático)
- Suporte a domínio customizado

### 5. Estrutura CSS

**Classes Principais:**
- `.shell` — Container wrapper (max-width, padding responsivo)
- `.section` — Seção padrão com padding
- `.section-alt` — Variação com cor de fundo alternada
- `.section-head` — Cabeçalho de seção (eyebrow, title, subtitle)
- `.link-arrow` — Link com seta animada (→)
- `.modal-backdrop` / `.modal-box` — Estrutura de modais
- `.accordion` / `.acc-item` / `.acc-head` / `.acc-body` — Accordions expandíveis

**Breakpoints Responsivos:**
- Mobile: base (< 768px)
- Tablet: 768px
- Desktop: 1024px+

### 6. Funcionalidades JavaScript

**Modais de Projetos:**
- `openModal(id)` — Abre modal específico
- `closeModalDirect(id)` — Fecha modal direto
- `closeModalOutside(event, id)` — Fecha ao clicar fora
- Dados hardcoded em objeto `projectData`

**Accordions:**
- `toggleAcc(element)` — Alterna estado expand/collapse
- Ícone dinâmico (+ / −)
- Primeiro accordion abre por padrão

**PDF Viewer:**
- `switchPDF(button, url)` — Troca URL do iframe
- Múltiplas abas de documentos por projeto
- Visualizador nativo do navegador

**Navegação:**
- Links anchor (#) para smooth scrolling entre seções
- Links auxiliares: WhatsApp, LinkedIn, E-mail

### 7. Fluxo de Dados

**Projetos:** Dados estruturados em objeto JavaScript + renderizados no HTML
**Formulário:** Form `#contato-form` com validação HTML5 (submit backend: em desenvolvimento)
**Navegação:** Links anchor para navegação entre seções
**Contato:** Integração direta com serviços externos (WhatsApp, LinkedIn, Gmail)

## Status

✅ Estrutura HTML completa e semântica
✅ Estilos CSS responsivos (mobile-first)
✅ Funcionalidades JavaScript (modais, accordions, PDF viewer)
✅ Acessibilidade formulário (IDs + autocomplete attributes)
✅ Integração com serviços externos (WhatsApp, LinkedIn, E-mail)
⏳ Backend formulário (em desenvolvimento)
⏳ Otimização de performance (lazy loading de imagens)
