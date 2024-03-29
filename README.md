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