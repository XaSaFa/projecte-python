# Formulari simple

Farem un programa en Flask que accedint a /form ens mostrarà un formulari amb un camp de text i un selector.

![image](https://github.com/user-attachments/assets/837e224d-728a-4eea-a734-4c3d06bb3534)

![image](https://github.com/user-attachments/assets/f4bc8d82-65c7-4fc9-8093-794e0d9d90c8)

![image](https://github.com/user-attachments/assets/06e1de01-1608-47c0-b282-ca38d3e06ba5)

## Codi Python

```
from flask import Flask, request

app = Flask(__name__)

@app.route('/form', methods=['GET', 'POST'])
def formulari():
    if request.method == 'POST':
        nom = request.form['nom']
        curs = request.form['curs']
        return f"Benvingut, {nom} del curs {curs}!"
    return '''
        <form method="POST">
            Nom: <input type="text" name="nom" required><br>
            Curs: 
            <select name="curs" required>
                <option value="1SMXA">Primer SMX, Grup A</option>
                <option value="1SMXB">Primer SMX, Grup B</option>
                <option value="2SMXA">Segon SMX, Grup A</option>
                <option value="2SMXB">Segon SMX, Grup B</option>
            </select><br><br>        
            <input type="submit" value="Enviar">
            </form>
        '''
```

# AMPLIACIÓ

1. Fes un formulari que demani un pes en Kg i el pugui transformar a lliures, tones o onces troy.
2. Fes un formulari que demani una velocitat en Km/h i la transformi a nusos o milles per hora.

3. Fes un formulari que pregunti la informació d'un personatge de Heroquest i **et retorni una fitxa de personatge omplerta** amb la informació de l'usuari:

![image](https://github.com/user-attachments/assets/f6ca7218-dc80-4a3d-af4f-2d01c706d468)

En aquest cas ha de preguntar:

- Tipus de Monstre o PNJ.
- Nom.
- Atac: 1 a 6.
- Defensa: 1 a 5.
- Moviment: 3 a 10.
- Cos: 1 a 10.
- Ment: 1 a 5.
- Habilitats especials.


 




