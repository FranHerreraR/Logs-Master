A continuación se realizara una revision detallada de algunos de los logs del PrecisionLanding:

## Log de inicio
El log que da inicio al servicio de Precision Landing
```
raspi-pl-dev 1628526245787 INFO root precisionLanding Precision landing service started
```

De acuerdo a la acción a realizar, se cambia al estado pertinente
## Log de Landing
Si se requiere aterrizar, cambia el estado a LANDING
```
raspi-pl-dev 1628526282500 INFO libs.service_state precisionLanding Changed service state to LANDING
```
## Log de Waiting
El estado default a la espera del request a aterrizar
```
raspi-pl-dev 1628526318876 INFO libs.service_state precisionLanding Changed service state to WAITING
```

## Aterrizaje Normal
```
raspi-pl-dev 1628526282501 INFO root precisionLanding Precision landing begin
```

```
raspi-pl-dev 1628526282519 INFO libs.drone_controller_coap precisionLanding DroneController: Drone connected
```

```
raspi-pl-dev 1628526287202 INFO root precisionLanding Precision landing started at: -36.793774 -73.055676 8.300000
```

```
raspi-pl-dev 1628526289372 INFO libs.controller_states precisionLanding Find: Landing pad found at (0.13693348147128212, 0.17665443757996527, 7.611397769390674, -1.2448657975940154)
```


