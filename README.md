# ✍️ Consejos para armar una charla de tecnología 
Estas notas tienen el propósito de ayudarte a pensar en cómo armar mejores charlas para la meetup. Vamos a mostrar brevemente cómo se puede estructurar una charla y contar qué cosas sí y cuáles no estaría bueno que tengan.

Dicho esto, el modelo que presentamos puede ser que no se aplique al tema que vos querés dar pero algunos conceptos son bastante generales y creemos que se pueden aplicar a cualquier tipo de charla.

Por último, esto que estás viendo es una versión beta de un proyecto que nos gustaría que sea más grande por lo que tus comentarios no solo son bienvenidos sino que nos encantaría escucharlos (y puede ser además que encuentres algunos errores o cosas mejorables).


## ⚒ Cómo estructurar la charla
Siempre tenemos que hacer todo lo posible por ser claros y predecibles con nuestra audiencia. Es decir: decir al principio sobre qué vamos a hablar, hablar sobre eso y después hacer un resumen de sobre qué hablamos. (Como ya aclaramos en la introducción puede ser que este modelo no se aplique a todas las charlas pero sí al 99% de los casos, así que tratá de usarlo. Te va a ayudar a vos y a las personas que te estén escuchando).
En resumen, deberíamos poder estructurar nuestra charla siguiendo esta estructura:


### Intro: 

La intro tiene que servir para que la gente sepa qué esperar de la charla. Tenemos que poder contestar a estas dos preguntas:	

- Qué vamos a hacer.

- De qué conceptos vamos a hablar.


### Desarrollo:

El desarrollo es cuando desarrollamos lo que ya presentamos en la intro. Idealmente no deberíamos introducir ningún tema no hayamos dicho que íbamos a introducir. (En la sección siguiente: `Qué cosas sí y cuáles no incluir en la charla` vamos a ir en más detalle sobre cómo estructurar esta parte).
	
  
### Cierre: 

El cierre tiene que servir para resumir lo que vimos (le sirve a quiénes te están escuchando para ver si entendieron bien lo que trataste de explicar antes y te sirve a vos para introducir próximos pasos). Además nos permite (si queremos) agregar otros consejos, recursos y preguntas para que nuestra audiencia se pueda seguir preguntando cosas sobre el tema.


## ✅ Qué cosas sí y cuáles no incluir en la charla

*Cosas que sí*

* Un único concepto o un único tema: en Meetupjs las charlas tienen una duración máxima de 30 minutos por lo que, en este tiempo, no deberías tratar de explicar más de un concepto o tema. Te aconsejamos esto porque si tratas de explicarlo todo te va a pasar que no vas a tener explicando nada. Es preferible definir un único objetivo para tu charla y tratarlo en profundidad  (Ej: quiero que la gente se vaya sabiendo cómo armar un prototipo rápido de app en React)  a tratar de explicarlo todo y no terminar explicando nada (Ej: quiero mostrar toda la API de React para que todo el mundo vea todo lo que se puede hacer: ciclo de vida del componente, `state`, `props`, animaciones, eventos, etc).


* Orientar la charla a un proyecto o problema puntual: si sos programador/a seguramente sabés que la mejor forma de aprender algo es haciendo. Usando esta misma idea es que te aconsejamos que si vas a explicar un tema que posiblemente sea nuevo para la audiencia lo hagas usando un ejemplo de excusa o un pequeño proyectito que puedas ir retomando a lo largo de toda la charla. De esa forma, primero, te vas a poder ordenar vos (es más fácil darse cuenta de qué es importante mostrar y qué no cuando tenes que explicar cómo hacer algo), segundo, a quiénes te estén escuchando les va a resultar más fácil entender lo que querés explicar (Ej: no es lo mismo que yo te defina lo que son las `props` en React a que te diga un ejemplo puntual de cómo se usar).

* Usar recursos para explicar cosas complejas como ejemplos, analogías, repetición: cuando estás tratando de explicar algo complejo esta bueno que lo retomes muchas veces a lo largo de tu charla en diferentes momentos. Pero no es suficiente con que lo digas muchas veces. También es importante que lo vayas explicando de formas diferentes: con diferentes palabras, ejemplos, usando una analogía con otro lenguaje o tecnología, etc.

* Dejar conceptos afuera, pasar por algo algunos detalles de implementación o ser simplista con algunos conceptos: está bien no tratar de explicarlo todo, no profundizar mucho en la explicación de un concepto o explicar algo de una forma en que nos podrían acusar de set `not real developers`. Nuestro foco tiene que estar en cumplir el objetivo que nos propusimos con la charla (Ej: quiero que la gente se vaya sabiendo cómo armar un prototipo rápido de app en React). Es decir que todos nuestros esfuerzos tienen que estar puestos en cumplir esto y nos podemos permitir no darle tanta importancia a todos los demás conceptos que giran alrededor de esto. Por ejemplo, en este caso puntual, si bien es importante saber cómo setear nuestro entorno con Webpack nos podemos permitir pasarlo por alto porque lo que nosotros queremos que la gente se lleve es cómo hacer una app rápido en React.

*Cosas que no*

* Tratar de explicarlo todo.
* Mostrar una API entera.
* Mostrar partes de código que no se entiende de dónde salen.

## ⚡️ Un ejemplo de charla siguiendo esta estructura

### Ejemplo de charla: Introducción a React
**Proyecto: Armar un blog (crear y listar posts)**

#### Intro: 

_Qué vamos a hacer:_

* Crear las vistas del blog en JSX (lista de posts y edición de post).

* Popular una lista de posts en React.

* Guardar un post en una base de datos.
	
_Qué conceptos vamos a tocar:_

* Estructura de Containers y Components en React.

* Clases y funciones puras en React.

* Ciclo de vida del componente (`ComponentDidMount` y `ComponentWillUnmount`)

* JSX para crear la UI.

#### Desarrollo:

1) Creamos un componente que va a servir de vista para una nota del blog.

``` js
import React from ‘react’

const Post = props => {
	return (
		<div>
			<header>Lista de posts | Crear post</header>
			<section>
				<h1>Titulo del post</h1>
				<p>Contenido del post</p>
			</section>
		</div>
	)
}

```

2) Introducimos componentización mostrando que podemos extraer el `header` y convertirlo en un componente nuevo y después importarlo en esta vista.

``` js
import React from ‘react’

const Header = props => {
	return (
		<header>Lista de posts | Crear post</header>
	)
}

const Post = props => {
	return (
		<div>
			<Header />
			<section>
				<h1>Titulo del post</h1>
				<p>Contenido del post</p>
			</section>
		</div>
	)
}

```

3) Etc…

#### Cierre:

Cosas de las que hablamos:

* Cómo crear las vistas del blog en JSX.

* Cómo usar el state interno de un componente para almacenar posts.

* Cómo hacer operaciones asincrónicas en React.

* Cómo popular el state de React usando el ciclo de vida del componente.


Otras cosas para seguir pensando:

* ¿Qué desafíos se imaginan que surgen de hacer aplicaciones más grandes? (manejar un `state` más grande, tener más y más complejas operaciones asincrónicas o tener que reutilizar los componentes que generamos en más de una parte de la aplicación).

## 🕸 Un modelo que podés usar para organizar tus ideas mientras pensas la charla

Llenar esta estructura de charla seguramente te va a ayudar a organizarte a la hora de pensar la charla (igual todo el equipo de Meetupjs va a estar encantado de ayudarte a armar la charla o darte feedback si sentís que lo necesitas así que contáctanos frente a cualquier duda!).

*Intro:* 
  
- Qué vamos a hacer:
	
  - …
	
  - …
	
  - …
	
- De qué conceptos vamos a hablar:
	
  - …
	
  - …
	
  - …

*Desarrollo:*

(Tratá de ordenar en bullet points cómo va a ser todo el desarrollo de la charla, es decir, que vas a decir primero, qué después y así).

1) …

2) …

3) …

*Cierre:*

Qué vimos

-  …

- …

- …

Qué puede mi público seguir pensando/investigando para aprender más de este tema

- …

- …

- …

	









