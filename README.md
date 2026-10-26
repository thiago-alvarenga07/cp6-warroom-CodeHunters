# FICHA DE DECISÕES · War Room FiapBank (CP6 · 3 aulas)

> Este arquivo é o **README.md do repositório do grupo** (`cp6-warroom-<nome-do-grupo>`).
> Vale **5,0 pontos** (rodadas 0,5 · relâmpagos 0,3), e a nota é pela
> **justificativa**, não pela letra. Preencham após cada aula e commitem até
> **23h59 do mesmo dia** (regras completas na seção 5 do enunciado).
>
> **Os incidentes da madrugada são revelados só em aula.** O título de cada registro
> será **ditado pelo professor na hora**; ninguém se antecipe.

**Grupo (nome da equipe plantonista):** CodeHunters

**Turma:** 2CCPG **Repo:** `cp6-warroom-CodeHunters`

**Integrantes (nome + RM):**

| Nome | RM |
|---|---|
|Thiago Sobral de Alvarenga | 562695|
|Pedro Miranda Campos Riato | 562117|
|Israel Karacsony de Camargo Nunes | 563435|
|Diego Antonio Silva Mendes | 565509|
|Giovanni de Lela Anjos Costa | 563066|
|Gabriel Hiro Nakamura | 562221|
---

## 📁 Dossiê técnico do FiapBank (MVP em produção)

**Stack:** Java 17 + Spring Boot + Spring Data JPA + Oracle. API com endpoints em
`/api/contas` e `/api/transferencias` (cenário visto desde a Aula 13).

**Contrato e regras de negócio que o banco prometeu aos clientes e aos reguladores:**

| Regra | Como deve ser |
|---|---|
| Transferência **PIX** | taxa **R$ 0,00** |
| Transferência **TED** | taxa fixa **R$ 5,00** |
| Saldo | **nunca fica negativo**: transferência/saque sem saldo é recusado com erro claro |
| Número de conta | **sequencial e único** (1001, 1002, 1003...), gerado pelo sistema |
| Extrato de transferência | grava **quem pagou** e **quem recebeu**, na ordem certa |
| CPF | **dado sensível**: nunca aparece nas respostas da API |
| Consultas ao banco | sempre parametrizadas, e cada operação **usa e libera** a conexão |
| Suíte de testes | roda antes de todo deploy; **verde** é pré-requisito pra subir |

**Como escrever a justificativa:** nomeie o **mecanismo técnico** em jogo (o
conceito das Aulas 11 a 15 que explica o incidente) e o **trade-off** (velocidade ×
segurança × faturamento × dívida). "Porque é mais seguro" não é justificativa.

---

# 📝 REGISTRO DE DECISÕES

> A cada incidente, o professor dita o título (ex.: "Rodada 1"). **Copiem o modelo
> abaixo, colem no fim desta seção** e preencham com o rascunho feito em aula, junto
> com o **placar do grupo** após a consequência. Commitem 1 commit por rodada até
> 23h59 do dia.
>
> **Eventos relâmpago:** registrem apenas se o grupo for **afetado** (o professor
> chama quem for; não ser chamado é bom sinal).

**Modelo (copiar para cada decisão):**

```
## <título ditado pelo professor>

**Tipo:** ( rodada / relâmpago ) · **Voto:** ( A / B / C / D )

**Justificativa:**

<2 a 3 linhas: mecanismo técnico + trade-off>

**Placar do grupo após esta decisão:** 🔥 __ · 💰 R$ __ mil · 🧹 __
```

*(as decisões entram aqui, na ordem em que a madrugada as trouxer; placar inicial:
🔥 7 · 💰 0 · 🧹 2)*
## Rodada 1: O saldo que virou negativo (19h12)

**Tipo:** (rodada) · **Voto:** ( C )

**Justificativa:**

Dentre todas as opções decidimos que a C é a ideal. A opção A não seria boa, pois o Hotflix não teria teste e remove o catch, que seria uma camada de segurança. Ou seja, seria muito arriscado; a opção B também não seria ideal, pois seria a opção que mais daria prejuízo financeiro; por fim, a opção D seria uma alternativa interessante, pois corrigiria esse bug, porém poderia voltar a uma versão com outros bugs.

**Placar do grupo após esta decisão:** 🔥 8 · 💰 R$ 35 mil · 🧹 1

## Evento relâmpago A: a busca que não acha ninguém(20h10)

**Tipo:** (relâmpago) · **Voto:** ( - )

**Justificativa:**

O grupo não foi afetado pela história pois não escolheu a alternativa que levava para esse evento

**Placar do grupo após esta decisão:** 🔥 8 · 💰 R$ 35 mil · 🧹 1

## Rodada 2: A injeção que derreteu o banco(21h02)

**Tipo:** (rodada) · **Voto:** ( A )

**Justificativa:**

Dentre as opções decidimos que a solução padrão e mais eficaz seria a alternativa A, pois ela separa o código dos dados por meio do input binding, neutralizando o ataque na raiz.

**Placar do grupo após esta decisão:** 🔥 8 · 💰 R$ 35 mil · 🧹 1

## Evento relâmpago B: as conexões que não fecham(22h40)

**Tipo:** (relâmpago) · **Voto:** ( - )

**Justificativa:**

O grupo não foi afetado pela história pois não escolheu a alternativa que levava para esse evento

**Placar do grupo após esta decisão:** 🔥 8 · 💰 R$ 35 mil · 🧹 1

## Rodada 3: A noite das contas gêmeas(22h50)

**Tipo:** (rodada) · **Voto:** ( C )

**Justificativa:**

Escolhemos a opção C pois ela permite identificar a origem e o impacto das duplicidades sem correr o risco de corromper ou alterar dados válidos. A partir da auditoria, pode-se definir a correção adequada e evitar decisões precipitadas.

**Placar do grupo após esta decisão:** 🔥 8 · 💰 R$ 45 mil · 🧹 1

## Rodada 4: O comprovante que aponta pra pessoa errada (00h47)

**Tipo:** (rodada) · **Voto:** ( B )

**Justificativa:**

Escolhemos a opção B, pois era a opção que mais transmitia transparência com o cliente. Não optamos pela alternativa A, pois o usuário só teria ciência que o erro foi corrigido após a realização de outro pagamento, na opção C, perderia muito tempo na comunicação com o consumidor, já na opção D, acreditamos que o problema apenas seria postergado.

**Placar do grupo após esta decisão:** 🔥 9 · 💰 R$ 70 mil · 🧹 0

## Rodada 5:  A fábrica que devolve null (01h30)

**Tipo:** (rodada) · **Voto:** ( A )

**Justificativa:**

Escolhemos a alternativa A, pois seria a opção mais rápida e objetiva para a solução do problema. Não optamos pela alternativa B, pois possui o risco de no futuro gerar outro problema ao cliente, a C, não escolhemos pois criaria outro problema a ser resolvido, já a D, acreditamos que não resolveria o problema e além disso o marketing da empresa seria prejudicado.

**Placar do grupo após esta decisão:** 🔥 8 · 💰 R$ 70 mil · 🧹 0

## Evento relâmpago C: o cadastro com metade dos campos (02h20)

**Tipo:** (relâmpago) · **Voto:** ( B )

**Justificativa:**

Escolhemos a alternativa B, pois com o builder com valores padrão, concentraria o default e validação no build, além de que é a única opção que não adicionaria construtores sobrecarregando os mesmos, e nem espalharia nulls pelo sistema.

**Placar do grupo após esta decisão:** 🔥 8 · 💰 R$ 70 mil · 🧹 0

## Evento relâmpago D: o teste verde que não testa nada (03h20)

**Tipo:** (relâmpago) · **Voto:** ( A )

**Justificativa:**

Escolhemos a alternativa A, pois acreditamos ser a opção mais honesta e ser a única que realmente resolve o problema. Não escolhemos as demais, pois a B não tem segurança, deixando propício ao depósito quebrar e ninguém ver, já a C acaba retirando a única camada de segurança do sistema.

**Placar do grupo após esta decisão:** 🔥 8 · 💰 R$ 70 mil · 🧹 0

## Rodada 6: O teste vermelho às 03h45 (a janela fecha às 04h)

**Tipo:** (rodada) · **Voto:** ( A )

**Justificativa:**

Escolhemos a alternativa A, pois é a única que cumpre o prazo sem perder a rastreabilidade. Como a janela fecha às 04h e a campanha abre às 08h sem exceções, então perder o deploy custaria muito no caso da B, já no C, esconde a falha no meio do ruído e normaliza deploy quebrado.

**Placar do grupo após esta decisão:** 🔥 8 · 💰 R$ 70 mil · 🧹 1

## Evento relâmpago E: "A taxa é 5 ou 50?" (05h58)

**Tipo:** (relâmpago) · **Voto:** ( C )

**Justificativa:**

Escolhemos a alternativa C, pois é a única opção que não possui algum risco de perda ou prejuízo financeiro, caso escolhesse B ou A, sem olhar o código e o contrato, ou sem fazer um teste antes, estaria dependendo de sorte para não ter um prejuízo.

**Placar do grupo após esta decisão:** 🔥 9 · 💰 R$ 70 mil · 🧹 1

## Rodada 7: Go/No-Go da Black Friday (06h15)

**Tipo:** (rodada) · **Voto:** ( B )

**Justificativa:**

Escolhemos a alternativa B, pois o bug mora no TransferenciaService (conta, taxa, extrato, saldo), então corrigir a causa e deixar a suíte verde custa só 2h de atraso, bem menos que erro financeiro em escala. Não optamos pela A pois abre sabendo que a TED cobra 10x e que o serviço é frágil, a C esconde um sintoma, e o PIX passa pelo mesmo serviço, já a D joga fora a campanha por um problema que se resolve em 2 horas.

**Placar do grupo após esta decisão:** 🔥 10 · 💰 R$ 110 mil · 🧹 0

---

## 🔎 O caminho do MEU grupo (preencher na 3ª aula, quando o mapa for revelado)

Uma linha por decisão registrada acima (usem os títulos ditados em aula):

| # | Decisão | Nossa letra | Consequência que ELA teria tido |
|---|---|---|---|
| R1 | Corrigir + escrever o teste (assertThrows) antes de subir | C | Demora 40 min a mais (8 clientes afetados no total), mas sobe com o assertThrows protegendo a invariante: a suíte ganha um teste honesto. |
| RA | Não participamos, pois escolhemos outra alternativa | - | - |
| R2 | PreparedStatement parameterizado | A | Parâmetros vinculados matam a injeção em ~40 min de madrugada |
| RB | Não participamos, pois escolhemos outra alternativa | - | - |
| R3 | Auditar as duplicatas antes de mexer no código | C | Antes de mexer: quantos clientes já são gêmeos? A auditoria leva a noite e revela extratos cruzados entre contas duplicadas; o fix só entra às 04h |
| R4 | Corrigir + reprocessar os extratos antigos | B | Corrige a gravação E reprocessa o histórico (~2h): os comprovantes já emitidos voltam certos; integridade total |
| R5 | Fail-fast: exceção clara na factory (tipo inválido) | A | A factory rejeita na hora com "Tipo de conta inválido: UNIVERSITARIA": o erro nasce e morre no mesmo lugar (~30 min) |
| RC | Builder com valores padrão | B | O Builder concentra defaults e validação no build() |
| RD | Adicionar o assert que falta (assertEquals/assertThrows) | A | 10 minutos e a suíte fica honesta |
| R6 | @Disabled no teste e subir na janela | A | Sobe na janela. O teste fica @Disabled("conferir taxa com o gerente"): alarme desligado. A taxa de R$ 50 segue no ar |
| RE | Reproduzir com um teste antes de responder | C | O teste dá evidência: a equipe entra no go/no-go sabendo da taxa |
| R7 | Corrigir o que a noite revelou + suíte verde, abrir 2h atrasado | B | Ao revisar o serviço, o time enxerga a taxa 50 e conserta antes de abrir: as 2h doeram menos que a taxa doeria. |

---

# 📋 PÓS-MORTEM · relatório de incidente (montar em sala na 3ª aula)

> Rascunho em aula e commit final `pos-mortem:` até 23h59 do dia da 3ª aula.

## 1. Linha do tempo da madrugada

Às 19h12, a equipe enfrentou um problema de saldo negativo e escolheu corrigir o código junto com a criação de um teste com assertThrows, protegendo a regra de negócio. Às 21h02, a equipe optou por utilizar PreparedStatement parametrizado para impedir ataques de SQL Injection. Às 22h50, decidiu auditar as contas duplicadas antes de alterar os dados, identificando extratos cruzados entre contas.

Às 00h47, a equipe escolheu corrigir a gravação e reprocessar os extratos antigos, recuperando a integridade do histórico. Em seguida, corrigiu o comportamento da factory para rejeitar tipos inválidos e adotou o Builder com valores padrão para centralizar a validação. Durante a madrugada, também corrigiu os testes para garantir que verificassem o comportamento esperado.

Às 03h45, a equipe decidiu desabilitar o teste que estava falhando para conseguir realizar o deploy dentro da janela, mantendo temporariamente o risco de uma taxa TED incorreta de R$ 50. Às 05h58, reproduziu o problema com um teste antes de responder. Finalmente, às 06h15, decidiu corrigir a causa do problema e garantir que a suíte estivesse verde, aceitando um atraso de duas horas para evitar prejuízos financeiros maiores.

## 2. Causa raiz de 2 incidentes (aula + mecanismo técnico)

**Incidente 1:** RODADA 1: O saldo que virou negativo (19h12)

Aula/mecanismo: Tratamento de exceções e testes automatizados com JUnit, especialmente assertThrows. A causa estava na ausência de uma proteção confiável para a regra de negócio que impede o saldo de ficar negativo. A solução foi corrigir a lógica e criar um teste que verifica se uma transferência sem saldo é recusada. O trade-off foi gastar mais 40 minutos para aumentar a confiabilidade e evitar prejuízos aos clientes.

**Incidente 2:** RODADA 2: A injeção que derreteu o banco (21h02)

Aula/mecanismo: Acesso seguro ao banco de dados com PreparedStatement e consultas parametrizadas. A vulnerabilidade ocorre quando entradas do usuário são concatenadas diretamente ao SQL, permitindo que sejam interpretadas como comandos. A parametrização separa os dados da instrução SQL e impede essa forma de injeção. A correção exigiu aproximadamente 40 minutos, um custo pequeno em comparação com os riscos de exposição de dados e comprometimento do banco.

## 3. O que faríamos diferente (2 rodadas + por quê)

Na Rodada 6, não desabilitaríamos o teste com @Disabled apenas para cumprir a janela de deploy. Embora essa decisão permitisse publicar a versão no prazo, ela desligou um alarme importante e manteve no ar a taxa TED incorreta de R$ 50. Priorizaríamos corrigir a causa e manter a suíte de testes válida, mesmo com atraso, para evitar cobranças indevidas em escala.

Na Rodada 3, manteríamos a auditoria antes de corrigir as contas duplicadas, mas buscaríamos automatizar a identificação de duplicidades e cruzamentos de extratos para reduzir o tempo de diagnóstico. A auditoria protege os dados válidos contra alterações precipitadas, enquanto uma investigação mais eficiente poderia diminuir o tempo até a correção definitiva.

## 4. A maior lição da equipe

A maior lição da equipe foi que na maioria das vezes nunca terá uma resposta 100% correta, mas sim uma que cause menos problemas para empresa, aprendemos também que na maioria das vezes a melhor decisão é priorizar a correção do problema, caso a resolução faça a equipe perder muito tempo, gerando muita consequência a melhor decisão seria voltar o código para uma versão anterior que ainda estava funcionando e resolver o problema logo em seguida e para evitar que uma warroom seja causada, devemos sempre realizar o máximo de testes possíveis para sempre evitar que aconteçam.
