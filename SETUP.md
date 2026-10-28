# Como colocar o perfil no ar / How to set it up

Estes arquivos vão no repositório especial **`tallecos/tallecos`** (o repositório com o mesmo nome do seu usuário — é ele que aparece no topo do seu perfil).

## 1. Estrutura dos arquivos / File structure

Coloque tudo assim, mantendo as pastas:

```
tallecos/                       (raiz do repositório)
├─ README.md
├─ assets/
│  └─ header.svg                (o banner animado — NÃO renomeie a pasta)
└─ .github/
   └─ workflows/
      └─ snake.yml              (gera a cobrinha automaticamente)
```

## 2. Enviar para o GitHub / Push

Pelo site: abra `tallecos/tallecos` → **Add file** → **Upload files** → arraste a pasta inteira → **Commit**.

Pelo terminal:

```bash
git clone https://github.com/tallecos/tallecos.git
cd tallecos
# copie README.md, assets/ e .github/ para cá
git add .
git commit -m "Novo perfil: banner animado, stats e cobrinha"
git push
```

## 3. Ligar a cobrinha / Enable the snake 🐍

A cobrinha só aparece depois que o GitHub Actions rodar uma vez:

1. No repositório, abra a aba **Actions** e, se pedir, clique em **I understand my workflows, enable them**.
2. Abra o workflow **"Gerar cobrinha das contribuicoes"** → **Run workflow** (botão à direita) para rodar na hora.
3. Espere ~1 minuto. Vai surgir um branch novo chamado **`output`** com os SVGs. A partir daí a cobrinha aparece no README e se atualiza sozinha todo dia.

> Se a imagem da cobrinha aparecer quebrada, é só porque o workflow ainda não rodou — faça o passo 2.

## 4. O que aparece sozinho / Shows up on its own

- **Contador de visitas, estatísticas e gráfico de atividade**: aparecem assim que o README estiver publicado e alguém abrir o perfil. Os números começam do zero e crescem com o tempo.
- **Banner** (`assets/header.svg`): já funciona de imediato, é um arquivo seu. Não depende de nenhum site externo.

## 5. Quiser ajustar depois / Tweaks

- **Cores dos cards**: todos usam o tema `tokyonight` para combinar com o banner. Dá para trocar por `radical`, `dracula`, `catppuccin_mocha`, etc., mudando `theme=` nas URLs do `README.md`.
- **Texto do banner**: me peça para regenerar o `header.svg` com outra frase, outro nome de destaque ou outras cores.
- **LinkedIn/e-mail**: já estão preenchidos com os dados que você passou.

---

Dúvida em qualquer passo? Me chama aqui no chat que eu ajusto. / Ping me anytime.
