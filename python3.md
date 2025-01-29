# Variables per URL

A Flask podem passar variables mitjançant una URL.

## Exemple passar nom d'usuari per variable

En aquest exemple passarem per url una variable que es diu username i té per valor xavi.

![image](https://github.com/user-attachments/assets/8bac7d45-6b8d-4fd0-b5ba-53e414c90538)

Per a fer-ho afegim la funció show_name:

```
@app.route("/user/<username>")
def show_name(username):
    return "<h1>Benvingut "+username+"!</h1>"
```

## Ampliació

1. Crea un programa al qual li passem una variable anomenada temp per url (amb un valor de temperatura en graus Celsius) i mostra per pantalla la temperatura en graus Celsius, Fahrenheit i Kelvin.
2. Generador de codis PIN: Crea un programa que rep per paràmetre una variable numèrica anomenada longitud i crea un codi numèric de nombres aleatoris de la longitud passada per paràmetre.
3. Crea un programa que rep per paràmetre una variable anomenada quantitat que es una xifra d'euros i et diu quants bitcoins podries comprar amb aquella xifra.

