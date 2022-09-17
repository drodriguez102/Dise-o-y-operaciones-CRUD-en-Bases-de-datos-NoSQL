 Actividad 1 - Diseño y operaciones CRUD en Bases de datos NoSQL
Desarrollar el modelo de una base de datos MongoDb que permita la gestión de los participantes a un torneo deportivo, (deportistas, entrenadores, árbitros, encuentros deportivos, resultados y tabla de posiciones). Ustedes escogen el tipo de evento deportivo que deseen trabajar, el cual debe ser real y tener disponible los resultados y detalles del torneo deportivo.

DESARROLLO

 Requerimientos 
Se requiere una base de datos en donde se pueda almacenar la información del torneo de futbol entre diferentes sedes de una empresa, en total serán 5 equipos las cuales tendrán solo 1 encuentro con cada sede, al final se debe determinar:
	Equipos que pasan a la siguiente ronda.
	Tabla de puntos y goles anotados.
	Goleador del torneo.

 Reglas del torneo
	El ganador se llevará 2 puntos
	Si el equipo empata se dará 1 punto
	Si el equipo pierde no se dará puntos
	El ganador del torneo será el equipo con más puntos.


SOLUCION DE MODELO DE BASE DE DATOS
El modelo de datos tendrá que ser acorde con los datos de las siguientes colecciones (Deportistas, Entrenadores, Árbitros, Encuentros Deportivos, Resultados)

EQUIPO
Nombre	String
Numero Integrantes	Intenger

DEPORTISTA
Nombres	String
Apellidos	String
Altura	Intenger
Peso	Intenger
Edad	Intenger
Id 	Intenger
Equipo	ObjectId (Equipo)

ENTRENADOR
Nombres	String
Apellidos	String
Equipo	ObjectId (Equipo)
Id	Intenger

ARBITROS
Nombres	String
Apellidos	String
Id	Intenger

ENCUENTROS
Equipo A	ObjectId (Equipo)
Equipo B	ObjectId (Equipo)
Arbitro	ObjectId (Arbitro)
Nombre Encuentro	String

RESULTADOS
Encuentro	ObjectId (Encuentro)
Resultado	Intenger
Puntos	Intenger

TABLA DE POSICIONES
Equipo	ObjectId (Equipo)
Total Puntos	Intenger
Partidos Empatados	Intenger
Partidos Perdidos	Intenger
Partidos Ganados	Intenger

Después de realizado el torneo con los datos de resultado se podrá obtener la tabla de posiciones de cada encuentro y el ganador del torneo.
