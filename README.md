# vetra-marca

Fonte única da marca VETRA para pessoas e agentes de IA.

Quando a marca mudar, atualize aqui. O Hermes na VPS recebe a mudança com `git pull`, e o Design System no Claude é atualizado a partir destes arquivos.

## Conteúdo

```
vetra-marca/
├── Vetra-Guia-de-Marca.pdf        guia para gráfica, designer e parceiros
└── skills/
    └── vetra-brand/               skill no padrão SKILL.md (Hermes e Claude)
        ├── SKILL.md               regras resumidas e checklist de verificação
        ├── references/
        │   ├── guia-completo.md   guia de marca completo
        │   └── tokens.json        cores, tipografia, espaçamento e raios
        └── assets/
            ├── logos/             8 SVGs com texto em curvas
            └── fonts/             Manrope 400 a 800 + licença OFL
```

## Instalar no Hermes (na VPS)

O repositório é público, então o jeito mais simples é clonar e criar um atalho para a pasta de skills do Hermes.

```bash
# 1. Clonar
cd ~
git clone https://github.com/tiagomdemoraes/vetra-marca.git

# 2. Ligar a skill ao Hermes
mkdir -p ~/.hermes/skills/marca
ln -s ~/vetra-marca/skills/vetra-brand ~/.hermes/skills/marca/vetra-brand

# 3. Conferir
hermes skills list | grep vetra
```

Para atualizar depois:

```bash
cd ~/vetra-marca && git pull
```

Para manter sempre em dia, agende o `git pull` no cron da VPS (por exemplo, a cada hora).

## Usar

No Hermes: "use a skill vetra-brand e crie um post de carrossel sobre ...".
No Claude: peça para usar o design system "Vetra".

## Regras do repositório

- Não edite os SVGs à mão. Logo novo só depois do refinamento do designer.
- Toda mudança de regra entra primeiro no `SKILL.md` e no `guia-completo.md`, juntos.
- Fonte Manrope sob licença SIL Open Font License (ver `assets/fonts/OFL.txt`).
