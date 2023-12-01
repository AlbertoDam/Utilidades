# Guia de elementos react native y sus instalaciones.
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>


## Índice


<ol>
  <li> <a href = "#Tab-Navigation"> Tab-Navigation </a> </li>
  <li> <a href = "#Icons"> Icons </a> </li>
  <li> <a href = "#commit"> Commitear cambios </a> </li>
  <li> <a href = "#push"> Subir cambios </a> </li>
  <li> <a href = "#pull"> Descargar cambios </a> </li>
  <li> <a href = "#log"> Mostrar logs de los push realizados con su ID </a> </li>
</ol>



<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>

<br> <br>

<span id="Tab-Navigation">

### Tab-Navigation. 

~~~

npm install @react-navigation/bottom-tabs

~~~

<span id="icons">

### Añadir iconos al proyecto

~~~
npm install --save-dev react-native-vector-icons
~~~
~~~
npm install @types/react-native-vector-icons
~~~
<p>
  Agregamos en el fichero: android/app/build.gradle ( cuidado!! no confundir con
android/build.gradle ) la línea:
</p>

~~~
apply from: file("../../node_modules/react-native-vector-icons/fonts.gradle")
~~~

<p>
  Si en lugar de todo el conjunto queremos un subgrupo ( que es lo recomendable ) ,
agregamos encima de la línea anterior, los que queremos:
</p>
~~~
project.ext.vectoricons = [
iconFontNames: ['MaterialCommunityIcons.ttf', ‘Ionicons.ttf’ ]
]
apply from: file("../../node_modules/react-native-vector-icons/fonts.gradle")
~~~

<span id="commit">

### Commitear cambios

~~~

git commit -m "Comentario"

~~~

<span id="push">

### Subir cambios

~~~

git push

~~~

<span id="pull">

### Descargar cambios

~~~

git pull

~~~

<span id="log">

### Mostrar logs de los push realizados con su ID
