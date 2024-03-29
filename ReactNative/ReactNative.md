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
   <li> <a href = "#Create"> Crear Proyecto React TS </a> </li>
  <li> <a href = "#Tab-Navigation"> Tab-Navigation </a> </li>
  <li> <a href = "#Icons"> Icons </a> </li>
  <li> <a href = "#Navigate"> Stack navigation y UseNavigate </a> </li>
  <li> <a href = "#Async"> Async Storage </a> </li>
  <li> <a href = "#Web"> WebView </a> </li>
  <li> <a href = "#drawer"> Drawer Navigation </a> </li>
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

<span id="Create">

### Crear Proyecto ReactNative TS 

~~~

npx react-native init NombreApp --template react-native-template-typescript
~~~

<hr>

<span id="Tab-Navigation">

### Tab-Navigation. 

~~~

npm install @react-navigation/bottom-tabs

~~~

<hr>

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
Si en lugar de todo el conjunto queremos un subgrupo ( que es lo recomendable ) ,
agregamos encima de la línea anterior, los que queremos:
~~~
project.ext.vectoricons = [iconFontNames: ['MaterialCommunityIcons.ttf', ‘Ionicons.ttf’ ]]
apply from: file("../../node_modules/react-native-vector-icons/fonts.gradle")
~~~

<hr>

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

<hr>

<span id="Async">

### Async Storage

~~~
npm install @react-native-async-storage/async-storage
~~~
<hr>

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
<hr>

<span id="drawer">

### Drawer Navigation (side menu).

~~~
npm install @react-navigation/native
npm install react-native-screens react-native-safe-area-context
~~~

Y luego modificar el fichero: android/app/src/main/java/nuestropackage/MainActivity.java
añadiendo:

~~~
import android.os.Bundle;
public class MainActivity extends ReactActivity {
 @Override
 protected void onCreate(Bundle savedInstanceState) {
 super.onCreate(null);
 }
}
~~~

despues instalar:

~~~
npm install @react-navigation/drawer
npm install react-native-gesture-handler react-native-reanimated
~~~

Y añadir import EN LA PRIMERA LINEA DEL ARCHIVO DEL DRAWER

~~~
import 'react-native-gesture-handler';
~~~

Si aún así falla añadir en babel.config.js dentro de modules.export:

~~~
plugins: ['react-native-reanimated/plugin']
~~~





