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
  <li> <a href = "#Navigate"> Stack navigation y UseNavigate </a> </li>
  <li> <a href = "#Async"> Async Storage </a> </li>
  <li> <a href = "#Web"> WebView </a> </li>
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

<span id="Navigate">

### UseNavigate y Stack

Navegacion:
~~~
npm install @react-navigation/native
~~~
~~~
npm install react-native-screens react-native-safe-area-context
~~~

Stack Navigation:

~~~
npm install @react-navigation/native-stack
~~~


<span id="Async">

### Async Storage

~~~
npm install @react-native-async-storage/async-storage
~~~

<span id="Web">

### WewView

~~~
npm install --save react-native-webview
~~~
Hay que agregar dos propiedades en android/gradle.properties:
~~~
android.useAndroidX=true
android.enableJetifier=true
~~~

<span id="log">

### Mostrar logs de los push realizados con su ID
