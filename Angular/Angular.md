### **ANGULAR**

- Crear un nuevo proyecto en angular sin los archivos de tests
```
g new todoapp --skip-tests
```
- Crear un nuevo componente
```
ng g component pages/home
```
Una vez creado el componente:
- 1 archivo HTML
- 1 archivo CSS
- 1 archivo TS
```
export class LabsComponent {

  welcome = 'Hello Todo App';
  tacks = [
    'Instalar CLI de angular',
    'Crear el primer proyecto',
    'Practica sostenida en el tiempo'
  ]
  age=25;
  name ="Rody Josue Ccoyllo Cule"
  address='La Florida'

}
```
Renderizando variables en el HTML -> **`{{ variable }}`**
```
<p>labs works!</p>
<h2>{{welcome}}</h2>

<ul>
  <li *ngFor ="let tack of tacks">
    {{tack}}
  </li>
</ul>
<br/>
<h3>{{'hello'.repeat(4)}}</h3>
<h2> La suma de 6+6 es: {{6+6}}</h2>
<h4>My name is {{name}} and have {{age}} years old. I am address is {{address}}</h4>
```

☣️Para usar las etiquetas especiales como `*ng for` debemos importar el `CommonModule`☣️

**Asignacion de valores a elementos HTML a traves de sus propiedades**


Existentes elementos HTML cuya asignacion de valores se realiza a `travez de sus propiedades`: 
-  <img  `src=""`  `alt=""`>
- <input `type="text"`>
- <button `disabled="true"`>Click Me </button_>

**`Property Binding`** Es la manera que dispone Angular para enlazar dinamicamente las variables del controlador  a las propiedades de los elementos de HTML. Para esto,se `utiliza los corchetes []`.
```
/*Controlador*/

  age=25;
  name ='Rody Josue Ccoyllo Cule'
  address='La Florida'
  avatar='https://josuecoder.github.io/pagina-personal/img/rody-josue-perfil.jpg'  

  person ={
    name: 'Rody Josue',
    age: 27,
    address: 'San Martin',
    avatar:'https://josuecoder.github.io/pagina-personal/img/rody-josue-perfil.jpg'
  }


```
```
/*HTML*/

<img [src]="avatar" alt="">
<input type="text" [value]="name">
<button disabled="true">Click Me</button>

<p>My name is {{person.name}}. I have {{person.age}} years old</p>
<img [src]="person.avatar" alt="">

```
 











