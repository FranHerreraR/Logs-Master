# Logs-Master
Acá se encuentra documetado todos acerca de los logs; formatos, modulos, etc

<img src="https://github.com/FranHerreraR/Logs-Master/blob/main/image.png" width="700" />

Esquema
<img src="https://github.com/FranHerreraR/logstash/blob/main/logstash.jpg" width="650" />

# Formato Logs-V 1.1
| Campo      | Descripción                                                                                                                               |
|------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| UUID       | Identificador unico del hardware sobre el que opera                                                                                       |
| Timestamp  | Timestamp en milisegundos del mensaje (11 digitos)-Formato UTC-0                                                                          |
| Componente | Nombre de la componente del log-EJ. adaptaodorDji                                                                                         |
| Modulo     | Nombre del modulo o clase relacionado con el proceso que se genero el log (*Puede ser class name +method name-*no debe contener espacios) |
| Tipo       | Tipo de mensaje: INFO, VERBOSE, ERROR, WARN                                                                                               |
| Mensaje    | Info. adicional. Puede contener espacios                                                                                                  |

*Ejemplo de Formato
  ** NOTA: campos van separados por espacios
 | UUID             |   | Timestamp   |   | Tipo |   | Modulo                |   | Componente   |   | Mensaje                     |
|------------------|---|-------------|---|------|---|-----------------------|---|--------------|---|-----------------------------|
| f24risdf430932sd |   | 11111111111 |   | INFO |   | virtualStickResources |   | adaptadorDji |   | Modo virtual stick activado |

# Cosas por investigar
* Metricas nuevas (bateria)
* Token seguridad
* RegEx Pattern log
