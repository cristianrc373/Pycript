# Pycript
Módulo Python compilado que permite la generación de claves asimétricas, cargar claves, cifrar y descifrar datos

Los requisitos necesarios para este módulo es tener instalado *cryptography* de Python.
El módulo consta de una sola clase llamada *Pycript*

## Pycript 🔑
Clase que crea aun objeto que permite generar nuevas claves RSA y cargarlas dentro del mismo, también permite encriptar y desencriptar listas y strings pasandolos como parametros y retornando los resultados.

### Funciones Pycript
```python
sq=Pycript()
#Por defecto el constructor de la clase no hace ninguna función.

sq.new_keys(size=4096)
#Función que crea un par de claves nuevas en el direcctorio "keys", creado en la misma ruta en la cual ejecutamos el código.

sq.charge_keys(dir="dir_prueba")
#Función que carga un par de claves "private_key.pem|public_key.pem" en el direcctorio indicado, hay que destacar que por defecto dir="keys".

sq.change_private("key.pem",dir="keys")
#Cambia o carga una clave privada indicada, en un direcctorio indicado, por defecto dir="keys".

sq.change_public("key.pem",dir="keys")
#Cambia o carga una clave pública indicada, en un direcctorio indicado, por defecto dir="keys".

sq.encrypt(["hola", "mundo"])
#Función que se encarga de cifrar los objetos que se pasan como parametro (de momento solo admite listas con string y números o strings y números).

sq.decrypt(objeto)
#Función que se encarga de descifrar los objetos que se pasan como parametro.
```
