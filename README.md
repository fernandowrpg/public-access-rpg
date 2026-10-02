# Public Access para Foundry VTT (v13 e v14)

Sistema não-oficial para jogar **Public Access** (PbtA) no Foundry VTT, com uma ficha de Latchkey automatizada.
Os textos dos moves básicos foram **resumidos** (não copiados) do livro. Cole o texto oficial no item se quiser.

> Sistema **não-oficial**, feito por fãs, sem vínculo com o autor de Public Access. O sistema não inclui o texto do livro; importe-o do seu próprio exemplar com o importador (veja abaixo).

## Instalação

**Pelo manifesto (recomendado):** no Foundry, vá em *Configuração → Sistemas de Jogo → Instalar Sistema* e cole no campo *URL do manifesto*:

```
https://github.com/fernandowrpg/public-access-rpg/releases/latest/download/system.json
```

**Manual:**

1. Baixe o `public-access.zip` da [última release](https://github.com/fernandowrpg/public-access-rpg/releases/latest).
2. Extraia em `{Dados do Foundry}/Data/systems/public-access`.
3. Reinicie o Foundry e crie um mundo usando o sistema **Public Access**.

- **Idiomas:** English e Português (Brasil).
- **Compatibilidade:** Foundry **v13 e v14**. No v14, o sistema usa o novo modo de mensagem (`messageMode`) e não transforma os cards em balões de fala.

Para publicar novas versões, veja [PUBLISHING.md](PUBLISHING.md).

## O que é automatizado

| Regra | Como funciona na ficha |
|---|---|
| **2d6 + habilidade** | Tiers: falha (≤6), 7–9, 10–11, 12+. O card mostra o texto do tier. No 12+ aparece também o texto do 10+, porque neste jogo o 12+ se soma a ele. |
| **Vantagem / desvantagem** | 3d6kh2 / 3d6kl2. As fontes **não se acumulam** e **se anulam**. |
| Vantagem pelo **Canto da Casa** | No diálogo de rolagem, escolha um item não marcado: ele dá vantagem e fica marcado. |
| Desvantagem por **Conditions** | Marque no diálogo as Conditions que atrapalham a ação. O Keeper também pode impor desvantagem. |
| **Virar uma Key** | Botão no card do chat: o resultado sobe um tier e o histórico da “linha do tempo descartada” fica registrado. Você escolhe entre a Key of the Child (qualquer ordem), a **próxima** Key of Desolation (sempre em ordem) ou a Key de um mistério. |
| Efeitos das Keys | `[unlock-dawn]` (ex.: The Sandstone Arch) desbloqueia e marca a Dawn Question “Signal from the Other Side”. `[retire]` (The Pure-White Signal) aposenta o Latchkey. |
| Prompts de Key pendentes | Cada Key marcada tem um toggle “resolvida”. O cabeçalho mostra quantas faltam, e há um lembrete no Dawn. |
| **4ª Condition** | “Receber Condition” com 3 slots cheios abre o diálogo de virar uma Key. |
| **Day / Night Move** | Pedem o que você teme. O move da fase atual fica destacado, e a ficha avisa quando você usa o move da fase errada. |
| **Meddling Move** | Pergunta como você está investigando. O 12+ lembra da fita Odyssey ou da história de Degoya. |
| **Nostalgic Move** | Sem rolagem. Escolha se você está relembrando ou ouvindo, o parceiro, o que Takes You Back e quais Conditions remover. Quem ouve ganha o lembrete da Pista. |
| **Answer a Question** | Pede a Complexidade, as pistas reunidas (avisa se forem menos que metade) e as pistas incorporadas: 2d6 + pistas − Complexidade, **nunca** com vantagem ou desvantagem. A Key só sobe o tier quando **todos** os Latchkeys viram uma. O card mostra quem já virou, e o Keeper pode forçar. |
| **Dawn Questions** | A primeira é sempre marcada. A desbloqueável é marcada ao ser desbloqueada. O limite é de 2 eletivas. O botão **Dawn** pergunta quais você respondeu “sim” e marca XP. |
| **XP e avanços** | São 6 caixas. Com a trilha cheia, **Avançar** zera o XP e marca um avanço. `[ability]` dá +1 em uma habilidade (máx. +3). `[move]` lembra de adicionar o move. |
| Fita em branco (Found Footage) | Item do Canto com “12+ automático”: marcá-lo antes da rolagem garante 12+. |
| Fase e fitas | Um **relógio de fases** flutuante mostra a fase atual para todos. O GM troca a fase clicando no relógio e ajusta as fitas Odyssey com +/-. Atalho **Shift+P**; o selo de fase da ficha abre o relógio. Também dá para mudar pelas configurações do sistema. |

## Compêndio de Latchkey moves

Os 20 Latchkey moves oficiais vêm prontos em dois compêndios, **Latchkey Moves (PT-BR)** e **Latchkey Moves (EN)**. Arraste um deles para a ficha. Cada Latchkey escolhe um no início do jogo, e o sistema avisa se outro Latchkey já tiver o mesmo move. Os textos são resumos; cole o texto oficial na descrição se preferir.

| Automação | Moves |
|---|---|
| +1 de habilidade ao adicionar (revertido ao remover, máx. +3) | Where's the Beef? (Vitalidade), A Winner is You (Presença), This is Your Brain (Razão) |
| Itens adicionados ao Canto da Casa | Robot in Disguise, Have You Ever Danced with the Devil, Say Hello to My Little Friend (o cachorro é **reutilizável** e nunca fica marcado) |
| Checkbox no diálogo de rolagem: **vantagem** | And They're Always Glad You Came, Just Say No |
| Checkbox no diálogo de rolagem: **12+ automático**, 1×/sessão | What Nintendon't |
| Checkbox no Meddling Move: **Pista extra, mesmo na falha**, 1×/sessão | They Think He's a Righteous Dude, You Never Know What You're Going to Get |
| Rolagem própria com **Presença** e textos de 10+ e 7–9 | Who Ya Gonna Call? |
| Nostalgic Move: botão para o parceiro receber **Sentindo-se Bem** (removível a qualquer momento para ter vantagem) | Thank You for Being a Friend |
| Pede um item e adiciona ao Canto da Casa | Strange Things are Afoot at the Circle K |
| Marcar The Chromatic Desert **fora de ordem** | I Am Error |
| Ignora a perda de Razão de The Fathomless Well | This is Your Brain |
| Usos **1×/sessão**, renovados pelo botão **Sessão** do Keeper | Come With Me If You Want to Live, Knowing is Half the Battle |
| Uso **1×/fase Day**, renovado quando o Keeper muda a fase para Day | Next Sunday A.D. |
| Lembrete a cada nova sessão | The Truth is Out There |
| Só envia o texto ao chat | Sight Beyond Sight e os demais sem rolagem |

**Botão Sessão** (só para o GM, no cabeçalho da ficha) renova os moves de uma vez por sessão. Também posta no chat os lembretes e as Keys pendentes de cada Latchkey.

Para regerar os compêndios a partir de `tools/latchkey-moves.mjs`:

```bash
npm i -D @foundryvtt/foundryvtt-cli
node tools/build-packs.mjs
```

## Importar os textos oficiais do livro

Os textos que vêm no sistema são resumos. Para ter o texto **idêntico ao livro**, copie do seu PDF e cole no importador. O texto fica só no seu mundo.

**Vários moves de uma vez** (Configurações → Configurar sistema → **Importar textos**):

1. Abra a folha de *Latchkey Moves* (ou as páginas de moves básicos do livro), selecione tudo e copie.
2. Cole no importador e escolha onde aplicar:
   - moves básicos (usados por todo Latchkey novo);
   - o compêndio **Latchkey Moves do Keeper**;
   - o diretório de Itens;
   - as fichas que já existem.
3. Cada move é reconhecido pelo nome no início de uma linha:
   - o texto completo vira a descrição;
   - o gatilho e os resultados (10+, 7–9, 12+, falha, “on a hit”) vão para o card do chat;
   - as automações (bônus, usos, vantagem…) são mantidas.
4. O relatório mostra o que foi atualizado e o que não foi encontrado.

**Um move só**: na ficha do move, use **Importar texto oficial**. Ali também fica o botão **Salvar no compêndio do Keeper**.

**Mistério**: na ficha do mistério, use **Importar texto oficial** e cole a ficha inteira.
- As seções são achadas pelos títulos: PRESENTING THE MYSTERY, QUESTIONS & OPPORTUNITIES, a Key, MOMENTS, a ameaça, DANGERS, LOCATIONS, SIDE CHARACTERS, CLUES e REWARDS.
- Dá para colar **uma seção por vez** escolhendo-a no diálogo.
- Antes de aplicar, o importador mostra quantos itens encontrou.
- Pistas encontradas, Locations visitadas e Recompensas resgatadas são preservadas.

Os compêndios **Latchkey Moves do Keeper** e **Mistérios do Keeper** são criados no mundo, dentro das pastas do sistema. O de moves já vem com os 20 moves e suas automações, pronto para receber os textos. Atualizações do sistema não mexem neles.

## Mistérios

### Organização dos compêndios

```
Public Access
├── Latchkey Moves
│   ├── Latchkey Moves (PT-BR)
│   └── Latchkey Moves (EN)
└── Mistérios (Mysteries)
    ├── Mistérios (PT-BR)       ← The House on Escondido Street
    ├── Mysteries (EN)
    └── Mistérios do Keeper     ← compêndio do mundo, para os seus mistérios
```

- Os compêndios de mistério do sistema ficam **ocultos dos jogadores**, para evitar spoilers.
- O **Mistérios do Keeper** é criado automaticamente no mundo quando o GM entra. Ali você cadastra os seus mistérios, e eles não são sobrescritos por atualizações do sistema.

### Como cadastrar um mistério

1. Crie um Actor do tipo **Mistério**. Ou abra o compêndio **Mistérios do Keeper** e use *Criar entrada*.
2. Na ficha, clique no **lápis** para entrar no modo de edição e preencha:
   - Apresentação e pergunta para um Latchkey;
   - Perguntas (com Complexidade) e Oportunidades;
   - a Key do mistério e os Moments;
   - Ameaça central, “se ignorarem…” e Perigos (com regras especiais);
   - Locations (descrição, Paint the Scene, regra especial);
   - Side Characters (três detalhes, descrição, voz; “entra em jogo depois”);
   - Pistas e Recompensas.
3. Clique em **Salvar no compêndio do Keeper** para guardar ou atualizar o mistério no compêndio do mundo.

Para usar um mistério pronto, importe-o do compêndio (arraste para o diretório de Atores).

### Durante o jogo

| Onde | O que acontece |
|---|---|
| **Apresentar mistério** | Posta a apresentação, as Perguntas e a Key no chat e marca o mistério como **Ativo**. |
| **Answer a Question** | O diálogo lista as Perguntas dos mistérios ativos e preenche a Complexidade e as Pistas encontradas. No card, o Keeper clica em **Registrar no mistério** para marcar a Pergunta como respondida. |
| **Meddling Move** | Num acerto, o card mostra ao Keeper o botão **Revelar Pista**: ele escolhe uma Pista não encontrada dos mistérios ativos, que fica marcada com quem a encontrou e aparece no card. |
| **Virar uma Key** | A Key de cada mistério ativo aparece para todos os Latchkeys. Quando alguém a usa, ela fica marcada como usada no mistério. |
| Locations e Side Characters | Um clique posta a Location com a pergunta de Paint the Scene, ou apresenta o personagem no chat. Visitados e conhecidos ficam marcados. |
| Moments | Um clique posta o Moment no chat como narração. |
| **Recompensas** | **Resgatar** escolhe o Latchkey e marca quem resgatou. Se a recompensa for um item, ele entra no Canto da Casa; com `?`, o sistema pergunta o que é. |

## Latchkey moves customizados

Crie um Item do tipo **Move** (no diretório de Itens ou pelo **+** da ficha) e arraste-o para a ficha. Dá para configurar:

- **Categoria**: básico, Latchkey ou customizado (de mistério ou recompensa).
- **Rolagem**: habilidade escolhida na hora, habilidade fixa, só bônus, Answer a Question ou sem rolagem (só envia o texto ao chat).
- **Bônus fixo** e **vantagem ou desvantagem forçada**.
- Se permite **vantagem ou desvantagem** e se permite **virar Key**.
- **Usos limitados** (atual/máx.), com bolinhas clicáveis na ficha.
- **Marcar XP na falha**.
- **Gatilho**, **pergunta do diálogo**, descrição e **texto por tier** (falha, 7–9, 10–11, 12+).
- **Automação especial**: faz o move se comportar como Day, Night, Meddling, Nostalgic ou Answer a Question.
- **Move complementar**: aparece como checkbox ao rolar outro move (qualquer um ou um move básico específico) e dá vantagem, 12+ automático ou uma nota.
- **Renovação de usos**: manual, por sessão ou por fase Day.
- **Aumento de habilidade**, **itens concedidos** (prefixo `*` = reutilizável), **adiciona item ao usar** e **lembrete de sessão**.
- **Keys**: uma Key of Desolation que pode ser marcada quando quiser, ou uma cuja perda de habilidade é ignorada.

Atalhos:

- **Shift+clique** rola direto, sem diálogo.
- Arrastar um move para a **hotbar** cria uma macro.

## Modelo de ficha (importante)

O modelo já vem preenchido com as habilidades iniciais, as Key of the Child, as Keys of Desolation, as Dawn Questions e os avanços da ficha (com efeitos automatizados). Se quiser a redação exata da ficha impressa, cole as linhas no menu abaixo:

1. Como GM, vá em **Configurações → Configurar sistema → Modelo de Latchkey**.
2. Cole os textos da sua ficha impressa, uma entrada por linha:
   - Dawn: `!` = sempre marcada, `?` = desbloqueada por Key, sem prefixo = eletiva.
   - Keys: `Título :: texto`. Na Desolation, a ordem importa. Use as tags `[unlock-dawn]`, `[reduce:reason]` (−1 na habilidade) e `[retire]`.
   - O modelo padrão já traz as cinco Keys of Desolation conhecidas: Sandstone Arch, Wandering Monolith, Fathomless Well, Chromatic Desert e Pure-White Signal. **Confira a ordem e cole os textos** da sua ficha.
   - Avanços: `texto [ability]` ou `texto [move]`.
3. Todo Latchkey novo recebe esse modelo. Use **Salvar e aplicar a todos** para atualizar os já existentes.

Cada ficha também tem um **modo de edição** (ícone de lápis no cabeçalho) para ajustar as listas individualmente.

## API

`game.publicAccess` expõe:

- `useMove(actor, item)`
- `turnKey(actor)`
- `takeCondition(actor, nome)`
- `addXP(actor, n)`
- `setPhase("night")`
- `newSession()`
- `newMystery()`
- `exportMystery(actor)`
