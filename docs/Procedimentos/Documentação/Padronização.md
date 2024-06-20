  
## Estrutura de arquivos
- Cada produto deve possuir uma pasta nomeada com todas as letras maiúsculas dentro da pasta Produtos.

```bush
Produtos
    SKID    
    NEW PICCOLO
```

- As pastas que não são destinadas aos produtos devem ser nomeadas com a primeira letra maiúscula no plural.

```bush
Procedimentos
Documentos
```

- As subpoastas não destinadas aos produtos devem ser nomeadas com a primeira letra maiúscula no singular.

```bush
Procedimentos
    Documentação
    Projeto
```

- Dentro das pastas os arquivos devem ter a pimeira letra maiúscula no singular.

```bush
SKID
    Base.md
Procedimentos
    Documentação
        Introdução.md
```

## Macros
Para o uso das macros é necessário entender a sintaxe explicada na seção [MKDocs Macros](Introdução.md#mkdocs-macros).

Todos os nomes, links e imagens da documentação devem ser cadastradas como macros a fim de facilitar futuras manutenções e atualização.
Além desses itens toda e qualquer variável que será usada e pode ser alterada futuramente deve ser cadastrada como macro.

### Cadastro das macros
#### Nomeação dos grupos
Os grupos são um conjunto de variáveis de mesma natureza, são usados para organizar as macros de forma mais intuitiva.
Os grupos devem ser nomeadas com todas as letras minúsculas no plural de preferência com uma única palavra.

```bush
extra:
    nomes:
    links:
    imagens:
    .
    .
    .
```

#### Nomeação das variáveis
As variáveis são "apelidos" para os itens cadastrados para que sejam acessadas posteriormente em qualquer lugar da documentação.
As variáveis devem ser nomeadas com todas as letras minúsculas no singular e se preciso a separação de palavras deve ser feita pelo _ (underline).
O valor da variável é atribuído após o nome.

```bush
    nomes:
        perfil_viga: {{ nomes.perfil_viga }}
```

#### Imagens
Todas as imagens devem ser salvas na pasta **assets/imagens/**.
Os nomes das imagens não dedvem possuir espaços, use sempre *_* (underline) 
Os links para imagens devem seguir o padrão *HTML* para otimizar a utilização de recursos.

Os campos **largura** (width) e **altura** (height) são opcionais, se omitidos a imagem manterá o tamanho original.

```html
<img src='/assets/images/nome_do_arquivo.extensão' width='largura' height='altura'>
```
