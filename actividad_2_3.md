|   Logs   | ¿Qué imprimirá la consola? (Predicción) | Justificación Teórica (Usa términos como: Hoisting, Ámbito de bloque, Ámbito de función, Undefined,...) |
|  :---  |  :---  |  :---  |
| Log A  | Log A: undefined  | Antes de ejecutar producto = "Teclado Mecánico", su valor es undefined. |
| Log B  | Log B: Teclado Mecánico |  La variable producto contiene el valor "Teclado Mecánico" y se muestra correctamente. |
| Log C  | Log C: 25 | Las variables let tienen ámbito de bloque esta predomina sobre la variable descuento de fuera del bloque |
| Log D  | Log D: 10 | Fuera del bloque if, la variable descuento declarada con let deja de existir porque su ámbito de bloque ha terminado. |
| Log E  | Log E: ¡ERROR CATÁSTROFICO! | impuesto está declarado con const dentro de un bloque if. Al intentar usarlo fuera de ese bloque, no existe por su ámbito de bloque |
| Log F  | Log E: ¡ERROR CATÁSTROFICO! | precio está declarado con let y se intenta acceder a él antes de su declaración. Aunque existe hoisting, la variable está en la Temporal Dead Zone. |

1. Comprobacion

<img width="852" height="467" alt="Captura de pantalla 2026-10-06 120211" src="https://github.com/user-attachments/assets/03c46f33-9c81-4d8c-9db8-23bff11fe6cb" />

2. Conclusion

El uso de var en aplicaciones grandes es peligroso porque su hoisting puede provocar comportamientos inesperados.

LOG A: donde una variable existe pero contiene undefined, dificultando la detección de errores.

LOG E demuestran que los ámbitos limitados de let y const ayudan a aislar datos y evitar errores
