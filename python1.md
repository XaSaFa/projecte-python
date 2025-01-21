# Web Python 1 - Hola Món

Crearem un fitxer nou a Pycharm anomenat hello_world.py amb el següent contingut:

```
from flask import Flask

app = Flask(__name__)

@app.route("/")
def hello_world():
    return "<p>Hello, World!</p>"
```

![image](https://github.com/user-attachments/assets/dd0418ab-6b07-459c-9e8f-54f90bb0fa0e)

![image](https://github.com/user-attachments/assets/75cb7e03-a2ce-4427-b1b5-b01ee8d8991b)

I executem el programa dins del terminal de Pycharm amb la instrucció:

```
flask --app hello_world run
```

![image](https://github.com/user-attachments/assets/b92de0e4-b21f-45e8-b3b8-1b1e3ec99d10)

Com podem veure Flask ens diu que per accedir al nostre programa hem d'utilitzar l'adreça següent:

![image](https://github.com/user-attachments/assets/f667cda2-200b-4ae1-924c-5e110b9ec023)

Així que l'obrim al navegador i obtenim el resultat del nostre programa.

![image](https://github.com/user-attachments/assets/f5296cd7-adfd-4805-8d95-266c65a6c9c9)

Per finalitzar l'execució hem de tornar al terminal de Pycharm i prémer Control+C.

**Sempre que camviem el programa hem de parar l'execució i tornar a executar Flask per veure el nou programa en funcionament**

