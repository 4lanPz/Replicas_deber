# Replicas_deber
-Se importa las librearias que nos ayudaran a crear los documentos
y tambien las que nos permiten enviarlos documentos a la base de datos
con estos comandos
-(se debe tener instalado requests, couchdb y BeautifulSoup3)
import requests
from bs4 import BeautifulSoup
import couchdb
-se declara los valore de couch para indicar el servidor y la base de datos
couch = couchdb.Server('http://admin:admin@localhost:5984') esta es la url de mi mismo servidor
-si se usa otro como al momento de usar hamachi, hay que cambier y poner la contraseña
db = couch['datos_juegos']  # Cambia el nombre de la base de datos
-en esta variable se va a guardar los documentos
data = []
-aquí se indica el link y lo que se quiere buscar con ayuda de las librerias
con estas se indica que se quiere hacer en el link y luego que hacer con ese dato
en este caso se busca todas las etiquetas <a> de las paginas web de videojuegos
estas van a buscar los href, en donde estan los datos que vamos a guardar
estas se van a guardar con nombres y apellidos
-luego de indicar varios se va a mandar a la base de datos con libreria couchdb
