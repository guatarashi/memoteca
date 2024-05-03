# Memoteca

This project was generated with [Angular CLI](https://github.com/angular/angular-cli) version 14.2.13.

## Development server

Run `ng serve` for a dev server. Navigate to `http://localhost:4200/`. The application will automatically reload if you change any of the source files.

## Code scaffolding

Run `ng generate component component-name` to generate a new component. You can also use `ng generate directive|pipe|service|class|guard|interface|enum|module`.

## Build

Run `ng build` to build the project. The build artifacts will be stored in the `dist/` directory.

## Running unit tests

Run `ng test` to execute the unit tests via [Karma](https://karma-runner.github.io).

## Running end-to-end tests

Run `ng e2e` to execute the end-to-end tests via a platform of your choice. To use this command, you need to first add a package that implements end-to-end testing capabilities.

## Further help

To get more help on the Angular CLI use `ng help` or go check out the [Angular CLI Overview and Command Reference](https://angular.io/cli) page.

# Conteúdo curso
criação de componentes ->  ng g c <caminho onde será criado o componente>/<nome componente>
iniciar servidor -> ng serve 

## Aula 1

### O que aprendemos?<br/>
Instalar e utilizar o Angular CLI;<br/>
Criar uma aplicação Angular;<br/>
Estrutura da aplicação gerada pelo Angular CLI;<br/>
Criar e utilizar um componente Angular;<br/>
Inserimos a fonte, as cores e estilos.<br/>

## Aula 2

### O que aprendemos?<br/>
Criar componente de formulário para adicionar novos pensamentos;<br/>
Passar valores de uma propriedade do component para atributos de tag dentro do template com o uso de property binding;<br/>
Mostrar valores de propriedades do component no template por meio da interpolação;<br/>
Escutar eventos do template e fazer a chamada de métodos no component com o event binding;<br/>
Usar a diretiva ngModel que pertence ao FormsModule para a comunicação bidirecional entre component e template;<br/>
Como funcionam os diferentes tipos de comunicação entre component e template.<br/>

Criando formulário<br/>
Property Binding -> [value]="pensamento.conteudo"<br/>
<input
    type="textarea"
    class="input"
    id="pensamento"
    name="pensamento"
    placeholder="Digite o pensamento"
    [value]="pensamento.conteudo"><br/>

O property binding funciona no mesmo sentido da interpolação, unidirecional, vindo a informação do componente para o template. É representado pelo uso de colchetes em atributos de elementos HTML.

Property Binding -> {{ pensamento.conteudo }} -> interpolação<br/>
<div class="modelo modelo1 ff-roboto-mono">
    <img src="../../../../assets/imagens/modelo1.png" alt="Aspas azuis">
    <p class="conteudo">{{ pensamento.conteudo }}</p>
    <p class="autoria"><b>{{ pensamento.autoria }}</b></p>
</div>
A interpolação permite a visualização do valor de uma propriedade do componente no template com o uso de chaves duplas. 
{{ nome-da-propriedade }}.<br/><br/>

Associando com Event Binding -> (click)="criarPensamento()"
<button (click)="criarPensamento()" class="botao">Salvar</button>

Two-way Data Binding (via de mão dupla) -> [(ngModel)]="pensamento.modelo" importar formsModule
<input
    type="radio"
    id="modelo3"
    value="modelo3"
    name="modelo-card"
    [(ngModel)]="pensamento.modelo"
>
Este binding combina o recurso do property binding e o event binding em uma única notação usando a diretiva ngModel.[(ngModel)]=”nome-da-propriedade”.

## Aula 3

### O que aprendemos?<br/>
Utilizar o RouterModule;<br/>
Utilizar a diretiva <router-outlet>;<br/>
Criar e configurar rotas;<br/>
Navegar por meio da propriedade routerLink.<br/>

## Aula 4

### O que aprendemos?<br/>
Tipos diferentes de diretivas;<br/>
Utilizar diretivas estruturais incluindo e excluindo elementos com ngFor e ngIf;<br/>
Utilizar expressões para estilizar elementos com ngClass.<br/>

### Para saber mais: tipos de diretivas
Diretivas de componentes: usado com um modelo. Esse tipo de diretiva é a mais comum.<br/>
Ex: <app-listarPensamentos>.

Diretivas estruturais: altera o layout do DOM adicionando e removendo elementos DOM.<br/>
Ex: NgIf, NgFor. NgSwitch.

Diretivas de atributos: altera a aparência ou o comportamento de um elemento, componente ou outra diretiva.<br/>
Ex: NgClass, NgStyle.

## Aula 5

comando -> "npm init -y" -> Esse comando cria o arquivo package json dentro da pasta backend
após isso instalar o json server comando -> npm i json-server
agora cria o arquivo db.json
após inserir os dados de teste no arquivo db.json, é hora de ir para o arquivo package.json
no arquivo package.json na tag scritps mude "test" para "start" e insera a seguinte informação -> "json-server --watch db.json --port 3000"
para iniciar o servidor json, execute o comando -> "npm start" dentro da pasta "backend"
interface(seria um bean no java) -> a interface serve para tipar a variavel, e o export é usado para que outras classes possam usar.
comando para criar service -> ng g s componentes/pensamentos/pensamento

### O que aprendemos?<br/>
Utilizar o JSON-Server simulando uma API REST;<br/>
Criar uma interface para definir tipos personalizados;<br/>
Entender a importância do Service e o novo decorator @Injectable();<br/>
Injetar dependências.<br/>

## Aula 6

Para verificar a versão atual do json-server instalada em seu sistema, você pode usar o seguinte comando no terminal:
json-server --version

Tendo confirmado que está com uma versão diferente; siga os passos abaixo para desinstalar a versão atual do json-server e instalar a versão 0.17.4:

Desinstalar a versão atual do json-server:
Abra o terminal e execute o seguinte comando:
npm uninstall -g json-server

Agora, você pode instalar uma versão específica usando o seguinte comando:
npm install -g json-server@0.17.4

### O que aprendemos?<br/>
Utilizar métodos de requisição HTTP com serviço HttpClient;<br/>
Utilizar o Observable no retorno dos métodos HTTP;<br/>
Capturar parâmetros em rotas;<br/>
Criar um CRUD.<br/>

# Curso: Angular 14: Evoluindo a Aplicação

## Aula 1

### O que aprendemos?<br/>

Criar um formulário reativo através da classe FormBuilder;<br/>
Associar o formulário criado no component ao template através da diretiva formGroup;<br/>
Utilizar a diretiva formControlName para associar os inputs do formulário;<br/>
Acessar os valores dos campos do formulário no template com o método get.<br/>

## Aula 2

### Expressões regulares
[Curso sobre expressões regulares](https://cursos.alura.com.br/course/expressoes-regulares)<br/>
[artigo sobre manipulação de strings e regex.](https://www.alura.com.br/artigos/javascript-replace-manipulando-strings-e-regex?_gl=1*sevuat*_ga*MTgyNzg2MzA3MC4xNjgzODk5ODI0*_ga_1EPWSW3PCS*MTcxNDc0MDg3NC4yMzguMS4xNzE0NzQyNTMxLjAuMC4w*_fplc*WUJCd0hJVUhjMjFRQUolMkJBVmUxTXY5U0wlMkJ1MDlGWW9aU3FjZ1RJUDYwNW5Rc0p4RDV2UXdZSmxiJTJGMzdRcWFHa2k1UXd6RVlGbGhVUnh0YlFrUE95eHZscTVneE4lMkJ3Q2FQaUpFNkNiQ1Q2TkhiNGltMG85QjMyUzN1aG44S0ElM0QlM0Q.)<br/>
[documentação angular validators](https://angular.dev/api/forms/Validators)<br/>
[validação de formulários reativos no Angular](https://www.alura.com.br/artigos/como-aplicar-validacao-formularios-reativos-angular?_gl=1*ktai3e*_ga*MTgyNzg2MzA3MC4xNjgzODk5ODI0*_ga_1EPWSW3PCS*MTcxNDc0ODYzMS4yMzkuMS4xNzE0NzUwODU5LjAuMC4w*_fplc*WUJCd0hJVUhjMjFRQUolMkJBVmUxTXY5U0wlMkJ1MDlGWW9aU3FjZ1RJUDYwNW5Rc0p4RDV2UXdZSmxiJTJGMzdRcWFHa2k1UXd6RVlGbGhVUnh0YlFrUE95eHZscTVneE4lMkJ3Q2FQaUpFNkNiQ1Q2TkhiNGltMG85QjMyUzN1aG44S0ElM0QlM0Q.)

### O que aprendemos?<br/>

Implementar validações nos campos do formulário através da classe Validators;<br/>
Identificar os tipos de erros que ocorreram nas validações;<br/>
Exibir mensagens de erro customizadas;<br/>
Mostrar mensagens de erro apenas quando o campo for acessado;<br/>
Habilitar/desabilitar o botão de salvar de acordo com o status do formulário.<br/>