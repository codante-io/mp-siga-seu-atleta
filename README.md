# Siga seu atleta | App Next.js fullstack

Nesse projeto vamos criar uma aplicação para dar visibilidade para os atletas paralímpicos e olímpicos do Brasil. A ideia é listar todos os atletas e suas contas do Instagram, filtrando por modalidades.


## 🤓 Antes de começar

Para essa aplicação, vamos usar dados reais dos atletas brasileiros. Esses dados foram coletados pelo time do Codante e estão disponíveis pra você em um arquivo `.sql`. Recomendamos que você utilize SQLite para a sua base de dados. Você pode utilizar o [plano gratuito do TursoDB](turso.tech) para isso.

## 🔨 Requisitos

### Crie uma Navbar
- Exibir a logo do projeto
- Exibir um link "Sobre"
   - Ao clicar nesse link, um modal deve ser aberto contendo um texto que descreve o projeto.

### Liste todos os atletas
- Ao entrar na página principal, uma lista dos atletas devem ser exibida.
    - Essa lista deve estar paginada com _infinite scroll_. Ou seja, quando o usuário rolar até o final da página, mais atletas devem ser carregados automaticamente até que todos os atletas sejam exibidos.
    - A lista deve vir ordenada do atleta com mais seguidores para o atleta com menos seguidores (os mais famosos antes)
- Para cada atleta, exiba seu **nome**, **número de seguidores**, **esporte**, **descrição**, **conta do Instagram** e **um link que redireciona para a página do Instagram**
    - O número de seguidores deve ser exibido no formato do Instagram.
        - Números entre 1 e 999 são exibidos normalmente;
        - Números entre 1000 e 9999 contêm uma vírgula, depois do milhar. Por ex: 9,345
        - Números entre 10000 e 999999 são abreviados com k. Por ex: 345k
        - Números acima de 1 milhão são abreviados com M. Por ex: 12M

### Implemente os filtros
- O usuário poderá pesquisar por texto pelo nome ou descrição dos atletas.
- O usuário poderá filtrar pela categoria do atleta: **olímpico**, **paralímpico** ou **todos**, sendo o padrão **todos**.
- O usuário poderá filtrar por um esporte dentro da lista de esportes disponíveis. Ao selecionar um esporte, apenas os praticantes daquela modalidade deverão ser exibidos.
   - Permita que o usuário digite o nome de um esporte para filtrar a lista de esportes disponíveis.. Por ex: se ele digitar "gin" exiba "ginástica artística" e "ginástica rítmica".
   - Exiba os pictogramas (logos) de cada esporte. Você pode consegui-los usando a [API das olimpíadas do Codante](https://docs.apis.codante.io/olympic-games).

### Implemente a ordenação
- Por padrão os usuários deverão ver os atletas do mais seguido para o menos seguido.
- Permita que o usuário troque a ordenação entre: **seguidores**, **nome** e **esporte**.
- Permita que o usuário altere a direção da ordenação entre: ascendente (do menor para o maior) e descendente (do maior para o menor). Por exemplo, a ordenação por seguidores pode começar com o atleta menos seguido (ascendente) ou com o mais seguido (descendente).

## 🎨 Design Sugerido

Temos uma sugestão de design no Figma. Entretanto, fique à vontade para montar a aplicação conforme a sua criatividade.

O design sugerido no Figma contém layouts básicos para a aplicação, incluindo a página inicial com a lista de atletas, filtros e a barra de navegação.

### Figma

🔗 [Link do design](https://www.figma.com/community/file/1408455704705137276)

## 👉🏽 Sobre esse mini-projeto

### O que você irá praticar:

Sugerimos que você faça esse projeto com Next.js e SQLite para o back-end.

Para conectar o SQLite com o Next, sugerimos o uso do Prisma.

Para os componentes, sugerimos o uso do shadcn/ui.

#### Next.js

- Pages, layout, server components e server actions
- Paginação, busca e filtros
- Componentes com shadcn/ui
- Infinite scroll (scroll infinito)

#### Prisma e SQLite

- TursoDB
- Criação de tabelas relacionais
- Implementação de filtros

### Pré requisitos

É interessante que você saiba Javascript, React e o básico do Next para fazer esse projeto.
