# Tok&Stok Store Theme

Tok&Stok Store Theme repositório dedicado a loja Tok&Stok.

## Índice

- [Fluxo de Desenvolvimento](#fluxo-de-desenvolvimento)
- [VSCode Plugins](#vscode-plugins)


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
