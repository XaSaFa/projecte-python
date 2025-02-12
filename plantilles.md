# Utilització de plantilles

[Link als apunts](https://dungeonofbits.com/utilizar-templates-con-python-y-jinja2.html).

## Instal·lació de jinja2

![image](https://github.com/user-attachments/assets/5db9141a-b921-40c0-9c77-acee410a97b3)

## Plantilla senzilla

```
from flask import Flask, request
from jinja2 import Environment, FileSystemLoader

app = Flask(__name__)

@app.route('/', methods=['GET', 'POST'])
def formulari():

    #Carrego la plantilla
    environment = Environment(loader=FileSystemLoader("templates/"))
    template = environment.get_template("hola.html")

    # Info conté la informació que paso a la plantilla
    info = {"nom":"Xavi","cognom":"Sancho"}
    # Paso la info a la plantilla per generar el document final
    textFinal = template.render(info)

    # Retornem com pàgina web el resultat final
    return textFinal
```

Contingut del fitxer hola.html

```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
</head>
<body>
    <h1>Hola {{ nom }}!</h1>
    Me n'alegro de veure'l senyor <b>{{ cognom }}.</b>
    
</body>
</html>
```

![image](https://github.com/user-attachments/assets/fe54bd70-04a2-4294-9acd-3bd80014c53e)

# Activitat

Prova el programa anterior i fes que un altre que mostri un formulari per pantalla per rebre de l'usuari els valors de nom i cognom.

El formulari haurà d'estar en un fitxer HTML anomenat formulari1.html.

Fitxer template1.py

```
from flask import Flask, request
from jinja2 import Environment, FileSystemLoader
app = Flask(__name__)
@app.route('/', methods=['GET', 'POST'])
def formulari():
    # L'usuari ha clicat a Enviar
    if request.method == 'POST':
        #Carrego la plantilla
        environment = Environment(loader=FileSystemLoader("templates/"))
        template = environment.get_template("hola.html")

        # Info conté la informació que paso a la plantilla
        nom = request.form['nom']
        cognom = request.form['cognom']
        info = {"nom":nom,"cognom":cognom}
        # Paso la info a la plantilla per generar el document final
        textFinal = template.render(info)

        # Retornem com pàgina web el resultat final
        return textFinal
        # Carrego la plantilla
    environment = Environment(loader=FileSystemLoader("templates/"))
    template = environment.get_template("formulari1.html")
    info = {}
    textFinal = template.render()
    # Retornem com pàgina web el resultat final
    return textFinal
```

Fitxer formulari1.html

```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
</head>
<body>
    <form method="POST">
        Nom: <input type="text" name="nom" required><br>
        Cognom: <input type="text" name="cognom" required><br>
        <input type="submit" value="Enviar">
    </form>
</body>
</html>
```

## Ampliació activitats

1. Fes una pàgina web utilitzant Bootstrap 5 que serveixi de plantilla per mostrar el full de personatge de Heroquest amb tot luxe de detalls.
2. Crea un programa que rebi la informació per a generar la fitxa de personatge de Heroquest i després mostri la web que acabes de fer en Bootstrap.
 
