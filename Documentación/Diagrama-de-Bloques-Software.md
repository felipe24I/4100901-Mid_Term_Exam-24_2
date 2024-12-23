# Diagrama de Bloques Software

![Software](https://github.com/user-attachments/assets/4fecda93-ff2f-419d-a03b-47e076a590cd)



## Descripción
Muestra el flujo de ejecución del software en el STM32F4 usando registros directamente:

### Inicialización
- **Configuración RCC**: Inicialización de relojes del sistema
- **Configuración GPIO**: Setup de pines para LEDs y botón
- **Configuración UART**: Setup de comunicación serial

### Loop Principal
- **Manejar Estado Puerta**: Control del LED indicador de estado
- **Procesar UART**: Lectura de comandos externos
- **Control LED Heartbeat**: 
   - Verificación de tiempo transcurrido (500ms)
   - Verificación del estado actual del LED
   - Toggle del LED según corresponda
   - Actualización del tiempo de referencia

### Interrupciones
- **ISR EXTI**: Manejo de interrupción del botón
   - Detección de pulsación
   - Actualización del estado del sistema
- **ISR UART**: Manejo de recepción de datos
   - Lectura de dato recibido

[Ver Diagrama](./assets/diagrama-bloques-software.png)
