<h1>Url's relativas al ContextPath en Thymeleaf</h1>

<p>Las URL's relativas al ContextPath son las relativas al directorio raíz (ROOT) de una aplicación web, una vez que están publicadas en el servidor. Las URL's relativas al ContextPath deben  iniciar
con "/" cuando vayamos a formar una URL para referenciar un recurso (imágenes, CSS, JS, PDF, vídeo, etc) en una aplicación. En un proyecto web cuando se utiliza Thymeleaf como motor de plantillas, los recursos estáticos deben guardarse en el directorio <b>src/main/resources/static</b>  </p> 

<p>Existen 3 maneras de incluir archivos JS y CSS a nuetro proyecto.
    <ol>
        <li> Incluimos los archivos vía CDN (Context Delivery Network), se utiliza la sintaxis estándar (sin expresiones Thymeleaf). Aquí podemos incluir librerías tales como: Bootstrap, JQuery, etc.</li>
        <li> Mediante archivos estáticos que deben guardarse en el directorio <b>src/main/resources/static</b> y se imbocan con la sintaxis Thymeleaf</li>
        <li> Mediante la inyección de dependencias directamente en el pom.xml (webjars)</li>
    </ol>
</p>


<h3>Formas más común de incluir archivos a nuestras plantillas Thymeleaf.</h3>

```html

<!--Para incluir archivos CSS en una vista se utilizaría: -->
<link rel="stylesheet" th:href="@{/css/bootstrap.min.css}" />
<link rel="stylesheet" th:href="@{/css/jquery-ui.min.css}" />


<!--Para incluir Imágenes (foto.png - jpg - otros) en una vista se utilizaría: -->
<img th:src="@{/images/spring.png}" alt="Spring logo" width="150" height="150"/>


<!--Para incluir archivos JavaScript en una vista se utilizaría: -->
<script th:src="@{/js/jquery-3.3.1.min.js}"></script>
<script th:src="@{/js/popper.min.js}"></script>
<script th:src="@{/js/bootstrap.min.js}"></script>
<script th:src="@{/js/jquery-ui.min.js}"></script>

```