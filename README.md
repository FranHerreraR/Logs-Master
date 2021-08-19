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

# Formato Logs-V1.2 json
Se mantiene el formato de campos de la versión 1.1, a excepción del contenido del campo Mensaje que puede derivar en más campos de interes dependiendo del modulo.
index: ""json-index"
Puerto: 5065
```
{"uuid":"f722c7e3a","timestamp":"1628632655144","Module":"example_module","Component":"example_component","example_field":example_value"}
```
* El formato de json debe ser:
```
"field": field_value -------- 
*En caso de string "field_value"--------En caso de que campo_value es de otro tipo (integer, float), no es necesario especificar el tipo.

* Los campos y valores de campo van separados por ',' y cada linea debe ir en '{ }':
'{ "field": field_value, ..., "Field_n": field_value_n }'
```
