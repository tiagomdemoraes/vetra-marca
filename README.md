# vetra-marca

Fonte única da marca VETRA para pessoas e agentes de IA.

Quando a marca mudar, atualize aqui. O Claude usa estes arquivos pela skill `vetra-brand`, e o Design System no Claude é atualizado a partir deles.

## Conteúdo

```
vetra-marca/
├── Vetra-Guia-de-Marca.pdf        guia para gráfica, designer e parceiros
├── guia-fonte/guia.html           fonte do PDF do guia
└── skills/
    └── vetra-brand/               skill no padrão SKILL.md
        ├── SKILL.md               regras resumidas e checklist de verificação
        ├── references/
        │   ├── guia-completo.md   guia de marca completo
        │   └── tokens.json        cores, tipografia, espaçamento e raios
        └── assets/
            ├── logos/             8 SVGs com texto em curvas
            └── fonts/             Manrope 400 a 800 + licença OFL
```

## Usar

No Claude Code, a skill fica ligada por atalho:

```bash
ln -s ~/Desktop/vetra-marca/skills/vetra-brand ~/.claude/skills/vetra-brand
```

Depois, peça: "use a skill vetra-brand e crie um post de carrossel sobre ...".
No Claude (app ou web): peça para usar o design system "Vetra".

## Regras do repositório

- Não edite os SVGs à mão. Logo novo só depois do refinamento do designer.
- Toda mudança de regra entra primeiro no `SKILL.md` e no `guia-completo.md`, juntos.
- Fonte Manrope sob licença SIL Open Font License (ver `assets/fonts/OFL.txt`).
