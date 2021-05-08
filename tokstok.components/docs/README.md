# Tok&Stok Store Components

Tok&Stok Store Components é uma coleção de componentes utilizado na loja Tok&Stok.

## Índice

- [Uso](#Uso)
  - [Styles API](#styles-api)
- [Lista de Componentes](#lista-de-componentes)
- [Criação de um novo componente](#criação-de-um-novo-componente)
  - [Estrutura do Projeto](#estrutura-do-projeto)
- [Fluxo de Desenvolvimento](#fluxo-de-desenvolvimento)
- [VSCode Plugins](#vscode-plugins)


## Uso

Este aplicativo utiliza o construtor de loja com a arquitetura de blocos da VTEX. 

Para saber mais sobre o Store Builder [clique aqui.](https://help.vtex.com/en/tutorial/understanding-storebuilder-and-stylesbuilder#structuring-and-configuring-our-store-with-object-object)

Para usar este aplicativo, você precisa importar em suas dependências em `manifest.json`.

```json
  "dependencies": {
    "tokstok.store-components": "0.x"
  }
```

Em seguida, você pode adicionar um bloco de componente ao tema do aplicativo, como fazemos com `exemplo-componente` em nosso component [__exemplo de componente__]().

Por exemplo, agora você pode alterar o comportamento do bloco `exemplo-componente` que está nos detalhes do produto. Veja um exemplo de como configurar:

```json
"exemplo-componente": {
  "props": {
    "showListPrice": true,
    "showLabels": false,
  }
}
```

### Styles API

Este aplicativo fornece algumas classes CSS como uma API para personalização de estilo.

Para usar esta API CSS, você deve adicionar o construtor `styles` e criar um arquivo CSS de estilo do aplicativo.

1. Adicione o construtor `styles` ao seu` manifest.json`:

```json
   "construtores": {
     "styles": "1.x"
   }
```

2. Crie um arquivo chamado `tokstok.store-components.css` dentro da pasta `styles/css`. Adicione seus estilos personalizados:

```css
.container {
   margem superior: 10px;
}
```

## Lista de Componentes

Abaixo, temos um README para cada componente deste projeto que explica como usá-los.

- [Exemplo Componente](exemplo-componente.md)

*Obs.: Sempre que criar um novo componente, adicione o README dele na pasta `docs` e atualiza esse README com o novo componente.*


## Criação de um novo componente

Para iniciar a criação de um novo componente, crie uma nova pasta em `react/components`. É onde seu código-fonte será armazenado. Crie também um novo arquivo js em `/react`, esse arquivo deve ser usado para expor seu componente, como:

### Estrutura do Projeto

Dentro de seu `react/components/<component_name>` você deve ter:

- index.js
- README.md (esse mesmo README deve estar na pasta `docs` também)
- [Optional] components/
- [Optional] constants/
- [Optional] utils/
- [Optional] queries/
- [Optional] mutations/
- [Optional] styles.css

Em seguida, dentro da pasta `react/` você precisa exportar seu componente, como:

```js
import ExemploComponente from './components/ExemploComponente/index'

export default ExemploComponente
```

Além disso, todas as dependências necessárias devem ser inseridas em `react/package.json`.


### Fluxo de Desenvolvimento

1. Faça o checkout na branch principal (main/master) ```git checkout master``` | ```git checkout main```

2. Atualize sua branch ```git pull```

3. Crie sua branch a partir da convensão `typetask/tasknumber-drecritive-name`
    typetasks: Fix | Feature | Release | Docs`
    ```git checkout -b feature/123-minicart```

4. Trabalhe em sua branch e faça commits periódicos. Evite (nunca) fazer commitássos épicos. Faça commits descritivos e fracionados, utilizando o [conventional commit](https://www.conventionalcommits.org/pt-br/v1.0.0/) ```git add --all && git commit -m "Feat: Commit message"```

5. Faça merges periódicos da branch principal na sua branch. Isso evita conflitos muito grandes e complexos. ```git merge master``` | ```git merge main```

6. Ao terminar, abra o PR seguindo o [template de PR](/.github/PULL_REQUEST_TEMPLATE.md) e selecione o líder da squad e 2 devs. O líder da squad é obrigatório a aprovação e só aprova o PR após outro dev já ter aprovado.
    6.1. Se o PR tiver conflitos, resolva-os antes de pedir avaliações.
    6.2. Se o PR tiver comentários/correções resolva todos os problemas antes de pedir uma nova avaliação.

7. Sucesso!

### VSCode Plugins
[Eslint](https://marketplace.visualstudio.com/items?itemName=dbaeumer.vscode-eslint) 

[Prettier](https://marketplace.visualstudio.com/items?itemName=esbenp.prettier-vscode)  

[EditorConfig](https://marketplace.visualstudio.com/items?itemName=EditorConfig.EditorConfig)

[Stylelint](https://marketplace.visualstudio.com/items?itemName=stylelint.vscode-stylelint) 
