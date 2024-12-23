# Diagrama de Componentes
![Componentes](https://github.com/user-attachments/assets/96af150e-3887-46de-94b8-a073c08c98a1)


## Descripción
Muestra la estructura interna del STM32F4 y sus componentes:

### Hardware Base
- **Core ARM Cortex-M4**: Procesador principal del sistema
- **Registros de Control**: Acceso directo a configuración de periféricos

### Periféricos
- **GPIOA**: Control de LEDs
- **GPIOC**: Control del botón de entrada
- **UART2**: Comunicación serial para comandos externos
- **SysTick**: Temporización del sistema
- **RCC**: Configuración de reloj del sistema

### Control de Aplicación
- **Control de LEDs**: Manejo de indicadores visuales
- **Control de Botón**: Entrada manual del usuario
- **Comunicación Serial**: Interfaz con YAT
- **Control de Tiempo**: Temporización de estados
