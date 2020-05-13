# JSdropz
Plugin in JavaScript / AJAX - Para carga de archivos
Version 1.0

# JS DropZ

Programa hecho en JS ; JQUERY

Como usar

### Importe los archivos de configuración a tu proyecto:

jsdropz.min.js
jsdropz.min.css

### Genere un form en tu <body>

- Action: Debes poner la dirección de tu API/Multpart que recibirá el archivo 
- Id: Es la id de identificación, tambien puede ser usada en una Class

#### Dentro del Form puedes usar inputs


Tus inputs llegaran normal a su api como $_POST
Y los archivos como $_FILES

Eso para PHP, pero puedes montar con cualquier otra lenguaje que soporte Multpart.

<form method="post" action="#apimultpart" enctype="multipart/form-data" novalidate id="jsteste" class="jsdropz"
    style="display: block; height:351px; ">
    <div class="jsdropz__input">
        <input type="file" name="archivo" id="file" class="jstesteinp" accept=".pdf, .jpg, .png"
            class="jsdropz__file" data-multiple-caption="{count} files selected" multiple style=" display:none;" />
        <center>
            <label for="file"><strong style=" cursor: pointer">Elige su archivo</strong><span
                    class="jsdropz__dragndrop"> o arrástralo
                    aquí</span>.</label>
        </center>
    </div>
</form>

## Codigo de activación

Codigo para que funcione su form.

#### opciones

- $() <- Defina su ID/Class a ser llamada con el formato Query.
- callback es una promesa con los datos de respuesta.

$("#jsteste").JSdropz({
    callback: function (ajax, data, respuesta) {
        console.log(ajax);
        console.log(data);
        console.log(respuesta);
    }
});


### Creado por Jonatan dos Santos. 05/2020
#### Bugs y colab (xjhonn@gmail.com)