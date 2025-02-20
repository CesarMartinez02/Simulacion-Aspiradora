
# Simulación Agente Aspiradora en NetLogo


Este modelo simula un robot de limpieza que se desplaza aleatoriamente en un entorno bidimensional, eliminando la suciedad presente en las celdas del mundo. El robot se mueve en direcciones aleatorias hasta que todas las celdas sucias han sido limpiadas.

## Estructura del Código

### Variables Globales
- `dirty-cells`: Cantidad total de celdas sucias.
- `steps`: Contador de los pasos realizados por el robot.

## Funciones Principales

### `setup`
Inicializa la simulación:
1. Borra el mundo previo.
2. Reinicia el contador de pasos.
3. Asigna suciedad a las celdas con una probabilidad del 33%.
5. Crea un único robot en el centro del mundo.
6. Reinicia el reloj de simulación.

### `go`
Ejecuta un ciclo de simulación:
1. Si no quedan celdas sucias, la simulación se detiene.
2. Aumenta el contador de pasos.
3. El robot revisa su celda actual y la limpia si está sucia.
4. Se mueve aleatoriamente en una de las cuatro direcciones posibles.
5. Avanza el tiempo en la simulación.

### `move-randomly`
- Determina una nueva dirección aleatoria (0°, 90°, 180°, 270°).
- Calcula las nuevas coordenadas.
- Si la nueva posición está dentro de los límites del mundo, gira y avanza.

### `lmx` y `lmy`
Funciones auxiliares para calcular desplazamientos en `x` y `y` según el ángulo de movimiento.

### `performance`
Devuelve la cantidad de pasos (`steps`) que tomó el robot para limpiar todo el entorno.

## Uso
1. Definir los valores de `n` y `m` antes de ejecutar `setup`.
2. Ejecutar `setup` para inicializar la simulación.
3. Ejecutar `go` para empezar la simulación.
4. En `performance` se obtiene la cantidad de pasos requeridos para limpiar toda el área.

## Notas finales
- El robot no sigue una estrategia óptima, ya que su movimiento es completamente aleatorio.
- Se puede modificar la probabilidad de suciedad en `setup` para ajustar la dificultad.
- Ampliar el tamaño del mundo (`n` y `m`) incrementa el tiempo de ejecución de la simulación.


Cesar Martinez, Mateo Pissarello, David Jimenez
