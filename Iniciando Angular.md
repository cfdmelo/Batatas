## Angular

#### Sobre:

Framework para desenvolvimento front-end baseado em componentes, que são módulos reutilizáveis que unem trechos de página, estilo e lógica em TypeScript.

**SPA - Single Page Applications** (Só precisamos reescrever parte do conteúdo da página, apenas uma página index.html que irá abrenger os outros components);

**NGC**- angular - gerar - component 

**NPM** - Node packages Modules (pasta node_modules)



#### Partes do projeto

**.gitignore** (partes do projeto que o git irá ignorar ao subir no repositório remoto, exemplo: dependências node_modules)

**angular.json** (contém todas as dependências do projeto) - na build alterar o "styles" e "scripts" para:

```
"styles": [
   "node_modules/ngx-bootstrap/datepicker/bs-datepicker.css",
   "node_modules/bootstrap/dist/css/bootstrap.min.css",
   "src/styles.css"
],
"scripts": [
   "./node_modules/jquery/dist/jquery.js",
   "./node_modules/popper.js/dist/umd/popper.min.js",
   "./node_modules/bootstrap/dist/js/bootstrap.js"
]
```

**index.html** (onde fica a formatação padrão do html "!" com o **<app-root>** no body, referencia da pasta **app**)

**app/app.component.ts** 

![alt-text](C:\Users\maari\OneDrive\Desktop\Bloco III\app.component.ts.PNG)

**Ver se tudo está instalado: **

- npm --version (se tem o gerenciador de pacotes pro Node.js)
- node --version (se tem o node)
- ng --version (angular)

**Instalar: **

- npm install -g typescript
- npm install -g @angular/cli

**Instalar BootStrap:**

- npm i bootstrap@4.5.3 *(bootstrap) * OU npm i bootstrap@latest

- npm install popper.js  *(JavaScript do Bootstrap)*

- npm install jquery@latest *(Jquery do BootStrap)*

- npm i ngx-bootstrap

- npm i ngx-order-pipe

  

*Em caso de erro na instalação do ngx-bootstrap :*

`npm install ngx-bootstrap`

ou

`ng add ngx-bootstrap (*yes*)`



#### Para rodar um projeto angular

`code .` para abrir o projeto no vscode

`ng new nomeProjeto` *(yes e depois CSS)* - para criar projeto Angular

`npm i`  para instalar

`ng serve` para rodar no servidor a aplicação

#### Iniciar projeto

`ng g c menu` ou outra pasta desejada, **para criar um component**

`<app-nomeDoComponent></app-nomeDoComponent>`, **para criar uma rota e rodar localmente**

### Rotas 

**Criar rotas para os componentes criados** 

- acessar app-routing-modules.ts 

- implementar o array const "Routes" com o exemplo a seguir:

  - ```
    {path: 'entrar', component: 'componentEntrar'},
    {path: 'cadastrar', component: 'componentCadastrar'}
    ```

  - antes das paths, é importante criar um path inicial, pra quando abrir aplicação, direcionar para determinado componente

    ```
    {path: '', redirectTo: 'entrar', pathMatch: 'full'}
    ```

  Traduzindo: quando o path for vazio, for iniciado por um localhost, ou ide, qualquer caminho que não seja um URL, irá iniciar pelo componente "entrar", o `pathMatch: 'full'` forçará a rota completa.

- no html dos componentes, ache o botão que referencia as rotas que deseja e acrescente como nos exemplos:

  - no entrar.component.html, no link "cadastre-se", acrescente:

    `routerLink="/cadastrar"`

  - no entrar.component.html, no link "cadastre-se", acrescente:

    `routerLink="/entrar"`

- no app.component.html use a tag `<router-outlet></router-outlet>`

# TypeScript

- Upgrade do JavaScript por ser fortemente tipado, diferente do JS
- Orientação a objetos
