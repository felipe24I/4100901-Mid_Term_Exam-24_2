# Diagrama de Flujo

![flujo](https://github.com/user-attachments/assets/f3f9371e-512a-44d7-9f52-5c07f02ac23d)



## Descripción
Muestra el flujo detallado del manejo del botón, sus interrupciones y eventos:

### Interrupción EXTI15_10_IRQHandler
- Detecta interrupción del botón
- Limpia bit pendiente
- Llama a la función de detección

### Función detect_button_press
- **Control de tiempo**:
   - Ignora rebotes menores a 50ms
   - Detecta presión simple si tiempo > 500ms
   - Detecta presión doble si tiempo entre 50-500ms
- Actualiza tiempo de última presión (b1_tick)
- Establece bandera button_pressed según el tipo de presión:
   - 1: Presión simple
   - 2: Presión doble

### Función button_driver_get_event
- Almacena estado actual de button_pressed
- Resetea la bandera button_pressed
- Retorna el evento capturado
