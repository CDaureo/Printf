# ft_printf

## Introducción

`ft_printf` es una implementación personalizada de la función `printf()` de la biblioteca estándar de C. Este proyecto es una excelente oportunidad para mejorar tus habilidades en C, trabajar con funciones variádicas y desarrollar código estructurado y extensible. Una vez completado, podrás incluir `ft_printf()` en tu `libft` para utilizarla en futuros proyectos.

---

## Requisitos Generales

- El proyecto debe estar escrito en **C**.
- Seguir la **Norma** de escritura de código establecida.
- Evitar errores como **segfaults, bus errors, double free**, etc.
- Liberar adecuadamente toda la memoria asignada en el **heap**.
- Proporcionar un **Makefile** que cumpla con las siguientes reglas:
  - `$(NAME)`, `all`, `clean`, `fclean`, `re`.
  - Compilar con `cc` y las flags `-Wall -Werror -Wextra`.
  - No hacer **relink**.
- Si se entregan **bonus**, estos deben estar en archivos separados `_bonus.{c/h}` y en una regla `bonus` del Makefile.
- Si se permite `libft`, esta debe incluirse en un directorio `libft` y compilarse antes del proyecto principal.

---

## Parte Obligatoria

### Nombre del programa
`libftprintf.a`

### Archivos a entregar
- `Makefile`
- `*.h`, `*/*.h`
- `*.c`, `*/*.c`

### Funciones autorizadas
- `malloc`, `free`, `write`
- `va_start`, `va_arg`, `va_copy`, `va_end`

### Uso de `libft`
**Sí** (opcional)

### Descripción
Debes reimplementar la función `printf()` de la biblioteca estándar de C con el siguiente prototipo:

```c
int ft_printf(const char *format, ...);
```

#### Consideraciones:
- No es necesario manejar el **buffer** interno de `printf()`.
- Se deben implementar las siguientes conversiones:
  - `%c` : Imprime un solo carácter.
  - `%s` : Imprime una cadena de caracteres.
  - `%p` : Imprime un puntero en formato hexadecimal.
  - `%d` : Imprime un número decimal con signo (base 10).
  - `%i` : Imprime un entero en base 10.
  - `%u` : Imprime un número decimal sin signo (base 10).
  - `%x` : Imprime un número hexadecimal en minúsculas (base 16).
  - `%X` : Imprime un número hexadecimal en mayúsculas (base 16).
  - `%%` : Imprime el símbolo de porcentaje (`%`).

### Creación de la Librería
- Se debe utilizar `ar` para generar `libftprintf.a`.
- El uso de `libtool` está **prohibido**.
- La librería debe generarse en la **raíz del repositorio**.

---

## Instalación y Uso

### Compilación
Para compilar la librería, simplemente ejecuta:
```sh
make
```
Para limpiar archivos objeto:
```sh
make clean
```
Para limpiar archivos objeto y la librería:
```sh
make fclean
```
Para recompilar todo:
```sh
make re
```
Si hay bonus disponibles, compilarlos con:
```sh
make bonus
```

### Uso en un Programa
Para utilizar `ft_printf()` en un programa C, inclúye el header y compila con la librería:
```c
#include "ft_printf.h"

int main()
{
    ft_printf("Hola, %s! Tu número favorito es %d.\n", "mundo", 42);
    return 0;
}
```
Compilación:
```sh
gcc -Wall -Wextra -Werror main.c libftprintf.a -o programa
```

---

## Consejos
- Divide tu código en **módulos** y funciones reutilizables.
- Utiliza **pruebas unitarias** para verificar la funcionalidad.
- Evita **memory leaks** utilizando herramientas como `valgrind`.
- Compara tu salida con la de `printf()` para verificar la exactitud.

---

## Autores
Este proyecto fue realizado como parte del programa **42**.

---

## Licencia
Este proyecto sigue las reglas del programa **42**, su distribución está sujeta a sus normativas.

