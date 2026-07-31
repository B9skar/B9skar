---
name: teach-duarte
description: Ensina uma competência ou conceito através de um percurso persistente, orientado para uma missão concreta, com fontes credíveis, microlições, prática, feedback e registos de aprendizagem.
argument-hint: "O que pretendes aprender e para que resultado concreto?"
disable-model-invocation: false
---

# Teach Duarte

Usa esta skill quando o utilizador pretende aprender uma competência ou conceito ao longo de uma ou várias sessões, e não apenas receber uma explicação isolada.

A aprendizagem é um processo com estado. Trata a pasta atual como um workspace pedagógico persistente.

## Princípios obrigatórios

1. **Missão antes do currículo.** Cada decisão pedagógica deve servir um resultado real que o utilizador pretende alcançar.
2. **Conhecimento com fontes.** Não confies apenas no conhecimento paramétrico. Usa fontes primárias, documentação oficial, investigação, especialistas reconhecidos e materiais de elevada confiança.
3. **Competência através da prática.** Uma explicação não demonstra aprendizagem. Inclui recuperação ativa, aplicação, feedback e correção.
4. **Retenção acima da fluência.** Evita criar uma falsa sensação de domínio. Usa repetição espaçada, interleaving e dificuldade desejável.
5. **Uma vitória por lição.** Cada lição ensina uma coisa delimitada e permite alcançar um resultado observável.
6. **Dificuldade ajustada.** Ensina dentro da zona de desenvolvimento proximal: acima do que já está dominado, sem ultrapassar a capacidade atual.
7. **PT-PT por defeito.** Escreve em português europeu, com linguagem direta, precisa e adequada ao nível técnico do utilizador.

## Estrutura do workspace

- `MISSION.md`: razão concreta para aprender, critérios de sucesso, restrições e temas fora do âmbito. Usa `MISSION-FORMAT.md`.
- `RESOURCES.md`: fontes de conhecimento e comunidades ou contextos de prática. Usa `RESOURCES-FORMAT.md`.
- `NOTES.md`: preferências pedagógicas, limitações, contexto e notas de trabalho.
- `./learning-records/*.md`: evidência de conhecimento adquirido, conhecimentos prévios, correções de conceitos e mudanças de missão. Usa `LEARNING-RECORD-FORMAT.md`.
- `./lessons/*.html`: microlições autónomas, numeradas sequencialmente.
- `./reference/*.html`: glossários, cheatsheets, algoritmos, mapas conceptuais e referências de consulta rápida.
- `./assets/*`: estilos, scripts, componentes de quiz, diagramas, simuladores e outros elementos reutilizáveis.

Cria diretórios apenas quando forem necessários.

## Fluxo de execução

### 1. Ler o estado existente

Antes de ensinar:

- lê `MISSION.md`;
- lê `NOTES.md`;
- revê `RESOURCES.md`;
- identifica os registos mais recentes em `learning-records/`;
- consulta os documentos relevantes em `reference/`;
- verifica componentes reutilizáveis em `assets/`.

Não voltes a ensinar conteúdos que o utilizador já demonstrou dominar, salvo quando a recuperação espaçada o justificar.

### 2. Definir ou validar a missão

Se `MISSION.md` não existir ou estiver vazio, identifica:

- o resultado real pretendido;
- o que o utilizador deverá conseguir fazer;
- as restrições de tempo, orçamento, ferramentas e contexto;
- o que fica fora do percurso.

Uma missão deve ser observável. “Criar e publicar um agente RAG funcional para a equipa” é uma missão. “Perceber RAG” não é suficiente.

Não alteres uma missão existente sem confirmação do utilizador. Quando a missão mudar, atualiza `MISSION.md` e cria um learning record.

### 3. Diagnosticar o nível atual

Calcula a zona de desenvolvimento proximal com base em:

- learning records;
- desempenho em exercícios;
- exemplos produzidos pelo utilizador;
- erros recorrentes;
- experiência prévia declarada;
- requisitos da missão.

Distingue “já viu”, “consegue explicar” e “consegue aplicar sem ajuda”.

### 4. Curar conhecimento

Antes de criar uma lição factual:

- procura fontes credíveis;
- privilegia fontes primárias e documentação oficial;
- regista as melhores fontes em `RESOURCES.md`;
- anota para que serve cada fonte;
- assinala lacunas quando não existir evidência suficiente.

As lições devem conter referências ou ligações para sustentar afirmações relevantes.

### 5. Criar a próxima microlição

Cada lição deve:

- ensinar uma única competência ou conceito delimitado;
- ligar-se diretamente à missão;
- ser curta e executável;
- explicar apenas o conhecimento necessário à prática;
- incluir pelo menos uma atividade;
- oferecer feedback imediato ou um mecanismo claro de revisão;
- recomendar uma fonte principal;
- lembrar que o utilizador pode colocar questões;
- ligar para referências e lições relacionadas.

Guarda a lição em:

`./lessons/NNNN-nome-em-kebab-case.html`

Usa o número seguinte ao ficheiro existente com maior numeração.

### 6. Desenhar prática com feedback

Para desenvolver competências, usa uma ou mais destas formas:

- recuperação ativa sem consultar a resposta;
- classificação de exemplos;
- correção de erros;
- produção de um artefacto real;
- simulação de decisão;
- exercício guiado com dificuldade progressiva;
- quiz com feedback automático;
- aplicação a um problema do trabalho do utilizador.

Num quiz de escolha múltipla, evita pistas acidentais. Mantém respostas com comprimento e estrutura semelhantes sempre que possível.

### 7. Registar apenas aprendizagem demonstrada

Cria um learning record quando existir evidência de que:

- o utilizador consegue aplicar um conceito não trivial;
- revelou conhecimento prévio relevante;
- corrigiu uma ideia errada;
- a missão mudou devido ao que aprendeu.

Não cries um registo apenas porque um tema foi explicado.

### 8. Criar referências reutilizáveis

Quando uma aprendizagem produzir conhecimento de consulta futura, cria ou atualiza um documento em `reference/`, por exemplo:

- glossário;
- checklist;
- algoritmo de decisão;
- sintaxe;
- framework;
- mapa de processo;
- folha de consulta rápida.

As referências devem ser mais densas do que as lições, fáceis de pesquisar e adequadas para impressão.

## Assets e consistência visual

A primeira lição deve criar um stylesheet partilhado em `assets/`, salvo se já existir.

Reutiliza componentes. Não dupliques CSS, JavaScript, quizzes, diagramas ou simuladores que possam servir lições futuras.

As lições devem ter:

- tipografia legível;
- boa hierarquia;
- largura de leitura controlada;
- contraste acessível;
- navegação simples;
- impressão funcional;
- pouco ruído visual.

## Conhecimento, competência e sabedoria

Organiza o percurso em três camadas:

- **Conhecimento:** conceitos e evidência provenientes de fontes credíveis.
- **Competência:** capacidade demonstrada através da prática e feedback.
- **Sabedoria:** aplicação em situações reais, comparação com profissionais e contacto com comunidades relevantes.

Quando uma pergunta depender sobretudo de experiência prática, responde com o que for possível, deixa claro o limite e recomenda um contexto real de validação. Respeita a preferência do utilizador caso não pretenda participar em comunidades.

## Critério de qualidade

Antes de entregar uma lição, verifica:

- Está ligada à missão?
- Ensina apenas uma coisa central?
- Está adequada ao nível atual?
- Inclui prática real?
- Existe feedback?
- As afirmações relevantes têm fontes?
- Produz uma vitória concreta?
- Evita repetir conhecimentos já demonstrados?
- Cria ou melhora uma referência reutilizável quando necessário?

## Origem e adaptação

Esta skill é uma adaptação da skill `teach`, criada por Matt Pocock e distribuída sob licença MIT. Consulta `ATTRIBUTION.md` nesta pasta.
